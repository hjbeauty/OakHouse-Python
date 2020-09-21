# Python Install 및 editmode

## - 파이썬 설치

> [http://www.python.org  ](http://www.python.org)

![](../../../.gitbook/assets/image%20%2826%29.png)

> 원하는 버전과 OS에 맞게 다운로드를 받는다  [https://www.python.org/downloads/](https://www.python.org/downloads/)

![](../../../.gitbook/assets/image%20%2885%29.png)

> * window 64비트일 경우는 “Windows x86-64 executable installer”
> * window 32비트일 경우는 “Windows x86 executable installer”
> * Mac OS X일 경우는 “Mac OS X 64-bit/32-bit installer”를 다운받는다
> * Linux일 경우는 기본적으로 파이썬\(Python\)이 설치되어 있을 것이므로 버전 확인 후 upgrade를 시키면 된 다

```text
$ python --version  또는 $ python —V
```

> 다운 받은 후  계속 next 누르면 된다 ,

![](../../../.gitbook/assets/image%20%2896%29.png)

> 1. add python path 체크해주면  환경변수에 path를 설정해준다.  
> 2. Install  now  클릭

![](../../../.gitbook/assets/image%20%2871%29.png)

![](../../../.gitbook/assets/image%20%28174%29.png)

![](../../../.gitbook/assets/image%20%2875%29.png)

![](../../../.gitbook/assets/image%20%28201%29.png)

> **윈도우 cmd 창을 켜서 아래의 명령어를 입력하여 버전을 확인한다**
>
> * \[window + R\]키를 눌러 “cmd” 콘솔 창을 열어서 실행
> *  python   --version
> * python에 관한 오류가 뜨면 위 화면에서  Add Python 3.7 to PATH를 체크 안해서 발생한것이다.    - 그러면, 시스템에서 환경변수를 추가해주면 다.

![](../../../.gitbook/assets/image%20%2858%29.png)

![](../../../.gitbook/assets/image%20%2843%29.png)

> cmd 창에서 python 실행

![](../../../.gitbook/assets/image%20%2817%29.png)

> 파이썬 명령행 실행 창

## - 파이썬을 시작하는  다양한 mode

### 1. 프롬프트 모드 \(즉시모드\) - REPL\(Read Evaluate Print Loop\) 

> "Python\(명령행\)"에 입력 하면 prompt 모드에서 인터프리터가 호출된다. Python 표현식을 직접 입력하고 Enter 키를 눌러 결과를 확인할 수 있다 
>
>  콘솔 화면에서 파이썬 구문을 입력하면 바로 결과를 반환하고 다시 입력할수 있는 도구

![](../../../.gitbook/assets/image%20%28223%29.png)

```text
>>>>'+' * 20 enter
```

![](../../../.gitbook/assets/image%20%28167%29.png)

> 함수를 만들어 사용할 수도 있다. 예\) add\(\)
>
> 바로직전 값을 받고 싶으면 \_ 를 입력하면 된

![](../../../.gitbook/assets/image%20%28127%29.png)

```text
종료하는 방법
exit() 또는 quit()  입력 
윈도우 : ctrl + Z
Mac , Linux : ctrl + D
```

## 2. 스크립트 모드

> 프롬프트모드도 가능하나 파일단위로 스크립트 모드로 할 수 있다

![](../../../.gitbook/assets/image%20%28200%29.png)

* 자동완성 모습 \(ctrl + space bar\)

![ctrl+spacebar&#xB97C; &#xB20C;&#xB800;&#xC744;&#xB54C; &#xC790;&#xB3D9;&#xC644;&#xC131;&#xD615;&#xC774; &#xC2E4;&#xD589;](../../../.gitbook/assets/image%20%2878%29.png)

> 스크립트파일 만들기

![](../../../.gitbook/assets/image%20%28214%29.png)

> 새로운 창이 나오면 다음과 같이 입력 후 F5번키를 눌러 실행한

![](../../../.gitbook/assets/image%20%2890%29.png)

![](../../../.gitbook/assets/image%20%28154%29.png)

## 3. 통합개발환경\(IDE\)

> 스크립트방식이나 다른 방식으로도 py을 만들어서 개발할 수 있지만 응용 프로그램 개발을 위해 프로그래머에게 코드 힌트, 구문 강조 표시 및 확인, 파일 탐색기 등과 같은 유용한 기능을 제공하는 소프트웨어로 중복 작업을 제거하고 응용 프로그램 개발에 필요한 시간을 크게 줄일 수 있다. 파이참이나 비주얼 스투디오 코드, 이클립스 등 으로 사용하는 것이 좋을 것이

