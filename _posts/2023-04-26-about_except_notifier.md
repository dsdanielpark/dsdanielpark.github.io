---
title: About ExceptNotifier 
author: Daniel Park
date: 2023-04-26
category: package
layout: post
---


The ExceptNotifier Python package offers a flexible approach to receiving notifications by enhancing Python's try-except statement. This package enables you to receive alerts through various messaging applications or emails.

With ExceptNotifier, you can obtain detailed compilation errors, including debug information, sent directly to your preferred messaging platform or email. By integrating OpenAI's ChatGPT, you can receive additional error code information as long as you provide the required API model name and key. This feature ensures that error handling and notifications are more informative and accessible, streamlining your debugging process.

- Related Project: ExceptNotifier
- Project Status: 2 Pre-Alpha
- Author: MinWoo Park
- Date: 2023-04

<br>

### Install 

```
pip install ExceptNotifier
```

### Official Github: 
<https://github.com/dsdanielpark/ExceptNotifier>

### Official Document: 
<https://exceptnotifier.readthedocs.io/en/latest/>


#### Dev Note
1. Applying ExceptNotifier in Python

    In Python, I use [sys.excepthook](https://docs.python.org/ko/3/library/sys.html#sys.excepthook) to call the ExceptNotifier by taking advantage of the interpreter calling `sys.excepthook` with three arguments (exception class, exception instance, traceback object) when an exception occurs. Since `sys.excepthook` is the highest-level exception handler that occurs just before the system shuts down, ExceptNotifier is implemented as a class that inherits from [BaseException](https://docs.python.org/3/library/exceptions.html) and overrides `sys.excepthook`. For overriding exceptions that cannot be raised or exceptions raised in threads, please refer to the sys.`unraisablehook()` function and the`threading.excepthook()` function, respectively.

2. Application of ExceptNotifier in IPython

    > Strictly, IPython is a package, not a programming language like Python, but it has been classified to aid understanding.
    
    IPython (Interactive Python) is a package consisting of a command shell for interactive computing for multiple programming languages.

    It is a very useful package that allows you to compile Python bit by bit in an interactive session through the concept of an interactive shell, but in IPython, control by `sys.excepthook` occurs just before the prompt is returned, so it is impossible to receive a traceback object using `sys.excepthook` and send an error message to each messenger app. Additionally, because it was necessary to inherit from BaseException, it was necessary to override other functions in IPython.

    Therefore, at first, I considered the [magics](https://ipython.readthedocs.io/en/stable/interactive/magics.html) in cell, but the problem of having to import the magic function every time in the cell can be cumbersome to use, so I decided to use the [set_custom_exc](https://ipython.readthedocs.io/en/stable/api/generated/IPython.core.interactiveshell.html) in IPython, which can work even by overriding it once. The `set_custom_exc` allows you to set a custom exception handler that is called when an exception in the exc_tuple occurs in the main loop (especially the `run_code()` method), and is designed so that the handle can return a structured traceback or None. Therefore, I can receive the traceback and send it to each messenger app. The order of top-level exception handling in IPython is different. You can use by `calling` raise in the `except` statement.

3. Using Environment Variables (environ) 

    In Python's except statement, it was designed to inherit `ExceptionBase`, so I thought about how to pass variables into the class and decided to set variables through `os.environ` to use them by distributing them as a package. Additionally, since the user's webhook URL or API key will not change, I named the variables in uppercase and set special names to prevent contamination from duplicate variables. Since the variables are used within the class, I added an underscore before the variable name.

4. About example code

    For explanation, in Python, the example uses the overrided `sys.excepthook` in the except statement, like `except ExceptTelegram as e:`. However, you can use it simply by overriding `sys.excepthook` once and calling `raise` in the `except` statement. In IPython, you can use `set_custom_exc` to override the `Exception` with a user-defined function once, and then call `raise` in the `except` statement to repeatedly take the desired ExceptNotifier action. Also, although the example uses` ExceptTelegram.__call__` or `SuccessTelegram().__call__()`, these are expressions to aid understanding, and you can change them to a more concise form if you prefer.


<br><br>

### 한국어

#### Except Notifier
Python 패키지 Except Notifier는 트레이스 백 된 오류 메시지를 포함하여 다양한 정보를 원하시는 메신저나 이메일을 통해서 발송해드립니다. 설치 후, 메시징 플랫폼이 요구하는 API나 Web Hook URL등을 환경변수로 설정하시면, try-except문을 통해 에러가 발생하였을 경우, 혹은 원하는 코드라인에서 자동으로 메시지를 발송할 수 있습니다.

또한 Open AI의 ChatGPT API를 통해 디버깅에 대한 힌트와 정보도 받아보실 수 있습니다.

#### 설치하기
```
pip install ExceptNotifier
```
#### 깃 허브 저장소
<https://github.com/dsdanielpark/ExceptNotifier>

#### 문서
<https://exceptnotifier.readthedocs.io/en/latest/>


#### 개발자 노트

- ExceptNotifier in Python

    예외발생시 traceback된 에러 메시지를 메신저나 메일로 발송하기위해 `sys.excepthook`에 오버라이딩하였습니다. Python 프로그래밍 실행 중 try-except문에서 예외 발생시 error class, error instance, traceback object를 인자로 받아 인터프리터가 `sys.excepthook`을 호출하는 것을 이용하였습니다. `sys.excepthook`이 시스템 종료 직전에 호출되는 최상위 예외 처리기이므로, ExceptNotifier는 `BaseException`을 상속받아 `sys.excepthook`에 오버라이딩할 수 있도록 구성하였습니다. 발생시킬 수 없는 예외 혹은 쓰레드에서 발생시킨 예외에 대한 오버라이딩은 각각 `sys.unraisablehook()`함수와 `threading.excepthook()`함수를 참조하여 비슷하게 구현할 수 있으나 이 경우는 고려하지 않았습니다. 
    
    *참조:* [sys.excepthook](https://docs.python.org/ko/3/library/sys.html#sys.excepthook)

- ExceptNotifier in IPython

    > 엄밀히 따지자면 IPython은 패키지로, Python과 같은 프로그래밍 언어는 아니지만 이해를 돕기 위해 분리하여 작성하였습니다.

    IPython(Interactive Python)은 Python을 통해 상호작용적인 컴퓨팅을 하기 위해 고안된 패키지입니다. IPython은
    Interactive Shell이라는 개념을 고안하여 대화식 세션으로 Python을 부분씩 컴파일할 수 있는 매우 유용한 패키지이지만, IPython에서는 Python과 다르게 `sys.excepthook`에 의한 제어가 프롬프트 반환 직전에 일어나게 되므로 `sys.excepthook`을 사용하여 트레이스백 객체(traceback object)를 받아 오류 메시지를 각 메신저 앱으로 발송하는 것(이하 ExceptNotifier의 "액션" 혹은 "목적"으로 칭함)이 불가능하였습니다. 또한 `excepthook`에 오버라이딩할 클래스는 반드시 `BaseException`을 상속받아야만 하는 Python의 규칙때문에, IPython에서는 `sys.excepthook`을 통해 ExceptNotifier의 액션을 취할 수 있도록 조정하기 어려웠습니다. 오류 발생 시 시스템 종료 순서, 호출되는 클래스와 메서드들이 상이하였기 때문에 다른 방법을 통해 ExceptNotifier의 목적을 달성하여야만 했습니다.
    처음에는 `magics`를 통한 구현(magic line)을 고려하였으나, 매번 셸에서 magic line을 반복하여 선언해 줘야 하는 번거로운 시나리오가 예상되었습니다. 목표한 패키지 유즈 케이스가 '사용자 부재 시 원격으로 Python 프로그램의 상태를 체크하는 것'이기 때문에 코드의 시공간적 효율이 다소 떨어지더라도 사용자 편의성에 집중하기로 결정하였습니다. 따라서, 한 번만 오버라이딩하여도 편하게 반복 사용할 수 있는 방법을 고민하였고, 사용자화할 수 있는 메서드들을 찾던 도중 `set_custom_exc`을 발견하였습니다. `set_custom_exc`는 메인 루프(특히 run_code() 메서드)에서 exc_tuple의 예외가 발생할 경우 호출되는 사용자 지정 예외 처리기입니다. `set_custom_exc`의 핸들러는 구조화된 트레이스 백 객체나 None을 반환하도록 설계되어 있으므로 트레이스 백 객체를 리턴 받는 프로세스 도중에 ExceptNotifier의 액션을 구현하였습니다. 
    
    *참조:*
    [magics](https://ipython.readthedocs.io/en/stable/interactive/magics.html), [set_custom_exc](https://ipython.readthedocs.io/en/stable/api/generated/IPython.core.interactiveshell.html), [BaseException](https://docs.python.org/3/library/exceptions.html)
    
- About Examples

     설명을 위해 Python에서는 예제에서는 ExceptTelegram과 같이 오버라이딩 된 `sys.excepthook`을 except문에서 호출하는 방식을 사용하였으나, `sys.excepthook`에 한번 오버라이딩한 뒤 간단히 except문에서 raise를 호출하여서 사용할 수 있고, Ipython에서는 `set_custom_exc`로 `Exception`에 사용자 지정함수에 한번 오버라이딩한 뒤 `except`에서 `raise`를 호출하는 것으로 원하는 ExceptNotifier의 액션을 반복해서 취할 수 있습니다. 또한, 예제에서는 `ExceptTelegram.__call__`혹은 `SuccessTelegram().__call__()`등을 사용하였으나 이는 이해를 돕기 위한 표현으로 더 간략하게 변경하여 사용하실 수도 있습니다.



- 환경변수

    Python의 except 문에서는 `BaseException`를 반드시 상속받아야만 하도록 설계되어있으므로, 클래스 안으로 변수를 전달할 방법을 고민하였고, 다양한 방법에 대해 실험을 수행하였습니다. 최종적으로 패키지로 배포하여 다양한 환경의 사용자들에게 제공하기 위해 `os.environ`을 통해 변수를 전달하여 재사용하기로 결정하였고, 시나리오상 사용자의 `WebHook URL`이나 `API Key`값을 자주 변경할 필요가 없으므로 대문자로 변수명을 표기하고, 중복되어 변수가 오염되는 것을 막기 위해서 특이한 이름으로 설정함과 동시에 클래스 내부에서 사용되는 변수이므로 변수명 앞에 _를 붙였습니다. 또한, Open AI의 API를 사용할지 여부 역시, 환경변수에 설정되어있는 변수명을 체크하는 간단한 조건문을 통해 불필요한 연산을 최소화하고자 하였습니다.

<br><br>

Copyright (c) 2023 MinWoo Park, South Korea <br>
All Copyright (c) Reserved.