---
title: About ExceptNotifier 
author: parkminwoo
date: 2021-08-10
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

한국어

1. ExceptNotifier Python

    파이썬의 경우 `sys.excepthook`을 사용하여, 예외가 발생하였을 경우 인터프리터가 3가지 인자(예외 클래스, 예외 인스턴스, 트레이스 백 객체)로 `sys.excepthook`을 호출하는 것을 이용하여 구현하였습니다. `sys.excepthook`이 시스템 종료 직전에 발생하는 최상위 예외 처리이므로, ExceptNotifier `BaseException`을 상속받아 `sys.excepthook`에 오버라이딩하기 위한 클래스로 구현하였습니다. 발생시킬 수 없는 예외 혹은 쓰레드에서 발생시킨 예외에 대한 오버라이딩은 각각 `sys.unraisablehook()`함수와 `threading.excepthook()`함수를 참조하시기 바랍니다. 

2. ExceptNotifier in IPython

    엄밀히 따지자면 IPython은 패키지로, 파이썬과 같이 프로그래밍 언어는 아니지만 통상적으로 이해를 돕기 위해 분류하여 작성하였습니다.
    IPython(Interactive Python)은 복수의 프로그래밍 언어에서 상호작용적인 컴퓨팅을 하기 위한 명령 셸로 구성되어있는 패키지입니다.
    Interactive Shell이라는 개념을 통해 대화식 세션으로 파이썬을 부분씩 컴파일할 수 있는 매우 유용한 패키지이지만, IPython에서는 파이썬과 다르게 `sys.excepthook`에 의한 제어가 프롬프트 반환되기 직전에 일어나게 되어있으므로 `sys.excepthook`을 사용하여 트레이스백 객체를 받아 오류 메시지를 각 메신저 앱으로 발송하는 것이 불가능하였습니다. 또한 `BaseException`을 반드시 상속받아야하였으므로 IPython에서는 `sys.excepthook`를 사용할 수 없었습니다.
    그래서 처음에는 `magics` function in cell을 고려하였으나, 매번 셀에서 magic line을 선언해줘야하는 문제가 발생할 수 있으므로 사용시 매우 번거로울 수 있다고 생각하였고, 결국 한번만 오버라이딩하여도 작동할 수 있도록, IPython의 `set_custom_exc`를 사용하기로 결정하였습니다. `set_custom_exc`는 메인 루프(특히 run_code() 메서드)에서 exc_tuple의 예외가 발생하는 경우 호출되는 사용자 지정 예외 처리기를 설정할 수 있으며, 핸들로는 구조화된 트레이스 백이나 None을 반환할 수 있도록 설계되어있으므로 트레이스 백을 리턴 받아 각 메신저앱에 발송할 수 있도록 하였습니다. `sys.excepthook`과 다르게 IPython에서는 최상위 예외처리의 순서가 다르므로, except문에서 raise를 호출하기만 해도 정상적으로 작동할 수 있습니다.

3. 환경변수

    파이썬의 except 문에서는 `BaseException`를 반드시 상속받아야만 하도록 설계되어있으므로, 클래스 안으로 변수를 전달할 방법을 고민하였고, 패키지로 배포하여 사용하기 위해서 `os.environ`을 통해 변수를 설정하기로 결정하였습니다. 또한 사용자의 WebHook URL이나 API Key 값이 자주 변하지 않을 것이므로 대문자로 변수명을 표기하고, 중복되어 변수가 오염되는 것을 막기 위해서 특이한 이름으로 설정함과 동시에 클래스 내부에서 사용되는 변수이므로 변수명 앞에 _를 붙였습니다.