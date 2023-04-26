---
title: About ExceptNotifier 
author: Daniel Park
date: 2023-04-26
category: Jekyll
layout: post
---

1. Applying ExceptNotifier in Python

    In Python, we use [sys.excepthook](https://docs.python.org/ko/3/library/sys.html#sys.excepthook) to call the exceptnotifier by taking advantage of the interpreter calling sys.excepthook with three arguments (exception class, exception instance, traceback object) when an exception occurs. Since sys.excepthook is the highest-level exception handler that occurs just before the system shuts down, exceptnotifier is implemented as a class that inherits from baseexception and overrides sys.excepthook. For overriding exceptions that cannot be raised or exceptions raised in threads, please refer to the sys.unraisablehook() function and the threading.excepthook() function, respectively.

2. Application of ExceptNotifier in iPython

    Strictly, iPython is a package, not a programming language like Python, but it has been classified to aid understanding.
    IPython (Interactive Python) is a package consisting of a command shell for interactive computing for multiple programming languages.

    It is a very useful package that allows you to compile Python bit by bit in an interactive session through the concept of an interactive shell, but in iPython, control by sys.excepthook occurs just before the prompt is returned, so it is impossible to receive a traceback object using sys.excepthook and send an error message to each messenger app. Additionally, because it was necessary to inherit from baseexception, it was necessary to override other functions in iPython.

    Therefore, at first, we considered the [magics](https://ipython.readthedocs.io/en/stable/interactive/magics.html) in cell, but the problem of having to import the magic function every time in the cell can be cumbersome to use, so we decided to use the [set_custom_exc](https://ipython.readthedocs.io/en/stable/api/generated/IPython.core.interactiveshell.html) in iPython, which can work even by overriding it once. The set_custom_exc allows you to set a custom exception handler that is called when an exception in the exc_tuple occurs in the main loop (especially the run_code() method), and is designed so that the handle can return a structured traceback or None. Therefore, we can receive the traceback and send it to each messenger app. Unlike sys.excepthook, the order of top-level exception handling in iPython is different, so just calling raise in the except statement can work properly.

3. Using Environment Variables (environ)
    In Python's except statement, it was designed to inherit exceptionbase, so we thought about how to pass variables into the class and decided to set variables through os.environ to use them by distributing them as a package. Additionally, since the user's webhook URL or API key will not change, we named the variables in uppercase and set special names to prevent contamination from duplicate variables. Since the variables are used within the class, we added an underscore before the variable name.

<br><br>

### ExceptNotifier 구현에 대하여

- ExceptNotifier Python

    예외발생시 traceback된 에러 메시지를 메신저나 메일로 발송하기위해 `sys.excepthook`에 오버라이딩하였습니다. 파이썬 프로그래밍 실행 중 try-except문에서 예외 발생시 error class, error instance, traceback object를 인자로 받아 인터프리터가 `sys.excepthook`을 호출하는 것을 이용하였습니다. `sys.excepthook`이 시스템 종료 직전에 발생하는 최상위 예외 처리이므로, ExceptNotifier는 `BaseException`을 상속받아 `sys.excepthook`에 오버라이딩할 수 있도록 구성하였습니다. 발생시킬 수 없는 예외 혹은 쓰레드에서 발생시킨 예외에 대한 오버라이딩은 각각 `sys.unraisablehook()`함수와 `threading.excepthook()`함수를 참조하여 비슷하게 구현할 수 있으나 이 경우는 고려하지 않았습니다. 
    
    *참조:* [sys.excepthook](https://docs.python.org/ko/3/library/sys.html#sys.excepthook)

- ExceptNotifier in IPython

    > 엄밀히 따지자면 IPython은 패키지로, 파이썬과 같이 프로그래밍 언어는 아니지만 이해를 돕기 위해 분리하여 작성하였습니다.

    IPython(Interactive Python)은 상호작용적인 컴퓨팅을 하기 위한 명령 셸로 구성되어있는 패키지입니다.
    Interactive Shell이라는 개념을 통해 대화식 세션으로 파이썬을 부분씩 컴파일할 수 있는 매우 유용한 패키지이지만, IPython에서는 파이썬과 다르게 `sys.excepthook`에 의한 제어가 프롬프트 반환되기 직전에 일어나게되므로 `sys.excepthook`을 사용하여 트레이스백 객체(traceback object)를 받아 오류 메시지를 각 메신저 앱으로 발송하는 것이 불가능하였습니다. 또한 `BaseException`을 반드시 상속받아야하였으므로 IPython에서는 `sys.excepthook`에서 ExceptNotifier의 액션을 취할 수 있도록 조정하기 어려웠습니다. 무엇보다 오류발생시 시스템 종류 순서와 호출되는 클래스와 메서드들이 상이하였으므로 다른 방법을 통해 ExceptNotifier의 목적을 달성하였습니다.
    처음에는 `magics` in cell을 고려하였으나, 매번 셸에서 magic line을 선언해줘야하는 번거로운 시나리오를 피하고자 한번만 오버라이딩하여도 작동할 수 있도록 작업하였습니다. `set_custom_exc`는 메인 루프(특히 run_code() 메서드)에서 exc_tuple의 예외가 발생할 경우 호출되는 사용자 지정 예외 처리기로 핸들러는 구조화된 트레이스 백 객체나 None을 반환할 수 있도록 설계되어있으므로 트레이스 백을 리턴 받는 프로세스 도중에 ExceptNotifier의 액션을 구현하였습니다. 위에서 설명한바와 같이 `sys.excepthook`과 다르게 IPython에서는 예외처리와 호출, 프로세스 중단 순서가 다르므로 한번의 오버라이딩 이후 except문에서 raise를 호출하기만해도 정상적으로 작동할 수 있습니다. 즉, Python에서 사용시는 ExceptTelegram과 같이 excepthook을 호출해주어야하지만 Ipython에서 set_custom_exc로 Exception에 사용자 지정함수를 한번 오버라이딩하면 그 다음부터 except문과 raise호출만으로도 원하는 ExceptNotifier의 액션을 취할 수 있습니다.

    *참조:*
    [magics](https://ipython.readthedocs.io/en/stable/interactive/magics.html), [set_custom_exc](https://ipython.readthedocs.io/en/stable/api/generated/IPython.core.interactiveshell.html)


- 환경변수

    파이썬의 except 문에서는 `BaseException`를 반드시 상속받아야만 하도록 설계되어있으므로, 클래스 안으로 변수를 전달할 방법을 고민하였고, 다양한 방법에 대한 실험을 수행하였습니다. 최종적으로 패키지로 배포하여 사용하기 위해서 `os.environ`을 통해 변수를 설정하기로 결정하였고, 시나리오상 사용자의 `WebHook URL`이나 `API Key`값을 자주 변경할 필요가 없으므로 대문자로 변수명을 표기하고, 중복되어 변수가 오염되는 것을 막기 위해서 특이한 이름으로 설정함과 동시에 클래스 내부에서 사용되는 변수이므로 변수명 앞에 _를 붙였습니다.