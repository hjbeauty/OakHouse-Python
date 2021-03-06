# function

#### 학습목표

1. 함수의 이해
2. 함수 구현 및 사용 숙지

#### 함수?

* 함수란 우리가 알고있는 개념처럼 주어진 입력\(input\)에 대해서 의도된 출력\(output\)를 전달하는 역할
*   > range 함수는 정수를 입력으로 전달하면 \[0, 정수\) 로 이루어진 리스트를 생성하는 역할
  >
  > sum 함수는 리스트, 튜플등을 입력으로 전달하면 전체 아이템의 합을 출력으로 전달하는 역할
  >
  > len 함수는 리스트, 튜플등을 입력으로 전달하면 아이템의 개수를 출력으로 전달하는 역할

### 

**함수의 정의**

* 정의 시 최초에 def 키워드 사용
* argument 정의 \(함수에 입력으로 전달하는 값을 의미, argument 또는 parameter라고 함\) 
* : \(콜론\) -&gt; 함수 역시 코드 블록이기 때문에 콜론\(:\) 필요
* body \(함수의 구현 부분, 함수 역시 코드 블록이기 때문에 들여쓰기 된 부분까지 함수의 코드블록으로 인지 함\)
  * 함수를 호출한 코드 \(caller\)로 함수가 해당 기능을 수행하고 완료된 값\(output\)을 전달하기 위해 return 키워드 사용
  * 즉, return 이후에 오는 값을 caller로 전달
* 함수의 네이밍 역시 중요
  * 즉, 어떤 기능을 하는 함수인지 이름으로 최대한 나타날 수 있게 해야함
  * e.g\) get\_a \(x\) get\_student\_name \(o\)

### 

**함수의 사용\(호출\)**

* 함수명\(파라미터1, 파라미터2, ... 파라미터n\)
* 위와 같이 정의 된 함수의 이름과 전달되는 parameter\(인자\)를 괄호안에 전달하여 함수를 호출
* 함수가 호출되면 실행의 흐름이 호출자\(caller\)에서 함수\(callee\)로 변경 됨
* 함수의 입력\(인풋\) 파라미터\(parameter\), 아규먼트\(argument\)라고도 함

### 

**함수 네이밍\(naming\)**

* 함수 이름으로부터 기능이 명시 
* 의미와 반대되거나 맞지 않는 이름은 사용금지



**parameter\(argument\) \(인자\)**

* 함수에 전달되는 입력\(input\)
* 입력이 필요하지 않을 수도, 1개의 입력만 있을 수도, 여러개의 입력이 존재할 수 도 있음
* 파라미터로 int, string, float, boolm, list, dict 등등 어떤 파이썬 객체도 전달 가능
* 심지어, 함수도 함수의 파라미터로 전달 가능
* python의 경우, 타입 명시가 없기 때문에, 함수 생성 시, 의도된 파라미터의 타입에 맞게 입력을 전달하는 것이 중요
* 또한 파라미터를 전달 할 때, 정의된 순서에 따라 값을 전달하는 것이 중요

### 

**Default parameter \(기본 인자\)**

* 함수의 파라미터에 기본값 지정 가능
* 파라미터를 명시하지 않을 경우, 지정된 기본값으로 대체



**Default parameter 사용 시 주의 점**

* 디폴트 파라미터 뒤에 일반 파라미터가 위치할 수 없음
* e.g\) 올바른 예

  > def test\(a, b, c = 1\)
  >
  > def test\(a, b = 1, c = 2\)
  >
  > def test\(a = 1, b = 1, c = 3\)

* e.g\) 올바르지 않은 예

  > def test\(a, b = 1, c\)
  >
  > def test\(a = 1, b, c\)
  >
  > def test\(a = 1, b = 1, c\)

### 

**keyword parameter \(키워드 파라미터\)**

* 파이썬의 경우, 파라미터에 값을 전달 할 때, 파라미터의 이름을 명시하여 전달 가능
* 파라미터 이름을 사용하지 않을 경우, 기본적으로 순서에 맞게 전달

```text
def add2(x=9 , y=10 ):
    return x+y


add2(y=300)
add2(y=300,x=23)
```

### 

**return \(리턴\)**

* 기본적으로 함수의 종료를 명시
  * return 옆에 값이나 수식이 있다면 해당 값을 호출자\(caller\)에게 반환\(전달\)
  * return 만 존재하면 None 반환
  * return이 없는 경우, 기본적으로 함수 코드 블록이 종료되면 종료로 간주. 이때도 None 반환

### 

**multiple return \(복수 값 반환\)**

```text
#  사칙연산 결과를 리턴하는 함수
def calc(x,y):
    add = x + y
    min = x - y
    mul = x * y
    div = x // y

    return add, min, mul , div
    
res1 = calc(3,4)
print(res1)
add, min, mul , div = calc(3,4)
print(add, min, mul , div)    
```

* tuple반환을 하여 복수개의 값 리턴 가능



**variable scope \(변수의 범위\)**

* 변수가 참조 가능한 코드상의 범위를 명시
* 함수내의 변수는 자신이 속한 코드 블록이 종료되면 소멸됨
* 이렇게 특정 코드 블록에서 선언된 변수를 **지역변수\(local variable\)** 이라고 함
* 반대로 가장 상단에서 정의되어 프로그램 종료 전까지 유지되는 변수를 **전역변수\(global variable\)**이라고 함 ==&gt; 
  * **global  변수명**
* 같은 이름의 지역변수와 전역변수가 존재할 경우, 지역변수의 우선순위가 더 높음

```text
num1 = 3
num2 = 4


def func( x , y ):
    global num1,num2
    print(num1,num2, x,y)
    num1 = x ** num1
    num2 = y ** num2
    print(num1,num2, x,y)

    # return num1 , num2
```

### 

**variable length argument \(가변길이 인자\)**

* 전달되는 파라미터의 개수가 고정적이지 않은 경우 사용
* e.g\)
  * print 함수
  * format 함수

> **\*args**, **\*\*kwargs**
>
> **\*args** : 파라미터를 튜플의 형태로 전달
>
> **\*\*kwargs** : 파리미터를 딕셔너리 형태로 전달\(네임드 파라미터\)

### **\*args**, 

```text
def myPrint(*x ):
    print(type(x))
    print(x)
    for item  in  x :
        print(item)
```

```text
myPrint(2)
myPrint(2,5,7,1)
myPrint()
```



**keyword parameter \(키워드 파라미터\) \*\*kwargs**

* \*\*가 붙은 경우에는 키워드 파라미터로 인식
* 즉 함수 호출 시, 파리미터의 이름과 값을 함께 전달 가능

```text
def myPrint2(**x ):
    print(type(x))
    print(x)
    for  k , v     in   x.items() :
        print("key:",k,'value:',v)

```

```text
myPrint2(param1=123)
myPrint2(key1=123, key2="kim")
```

* 가변길이 함수의 대표적인 예

  **문자열 포맷 함수**

  * 여러가지 값과 포맷을 이용하여 문자열을 정의할 수 있는 함수
  * {} placeholder를 문자열 내에 위치 시킨 후, 해당 위치에 format함수로 전달된 값으로 대체하여 문자열 생성
  * 포맷 구성은 다음 링크 참조 : [https://pyformat.info/](https://pyformat.info/)

