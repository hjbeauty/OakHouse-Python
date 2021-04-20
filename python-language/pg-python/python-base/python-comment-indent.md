# comment, indent, semicolon,backslash

## 0. 주석\(Comments\)

> 주석이란? 프로그램의 실행에는 전혀 관여하지않으면서 프로그램 코드 중간 중간에 코드에 대한 자세한 설명을 첨부하는것 
>
> * 메모를 남기고 싶을  때
> * 코드가 아니라는 표현 
> * 실행하지 않아야 할 문장
> * 프로그램의 가독성을 위한것으로 사람을 위한 문법

### - 주석의 종류

* 행단위 :  \#   , java : //
* 블럭단위 \(Document String\): """   ~~"""     , java : /\*~~ \*/  , /\*\*~~ \*/
*  **※ 주의 : 블록 주석은 중첩 불가**

```python
/**

매뉴얼작성시 필요한 주석 , 
**/

"""
매뉴얼작성시 """필요한 주석 , """
"""


```

![](../../../.gitbook/assets/image%20%28151%29.png)

## 1. 들여쓰기\(indent\)

> 가독성을 위해 들여쓰기를 한다 ,  자바에서 {} 을 사용하여 영역을 지정다. 하지만 파이썬은 들여쓰기를 사용하여 영역을 지정한다. 파이썬에서 들여쓰기란 문법적인 강제사항다.
>
> * if, for, class, def 등 작성시 코드 블럭을 구성하기 위해  : 다음 아랫 줄은 반드시 들여쓰기를 해야한다. 
> * 들여쓰기의 방법은 한칸, 두칸, 4칸, 탭 등 여러가지 방식이 있습니다.

```python
"""
들여쓰기 연습
---------------
"""
def line():
    """
    line 함수 : 30개의 -를 출력합니다.

    형식) line()
    """
    print("-" * 30)

def show(char="★", count=5):
    """
    show함수 :    지정문자를 지정한 갯수만큼 출력합니다.

    형식) showshow(char, count)
    첫번째 인수 : 출력한 문자(기본값  : ★)
    두번째 인수 : 출력할 개수(기본값 : 5)
    """
    print(char * count)
    line() # 이 줄의 들여쓰기 칸수를 변경해보세요!! 에러 확인

show()
show("◆")
# 인수에 기본값을 정해줬을 경우 뒤에서 부터 생략가능 : 30*5 = 150 출력
show(30)
show("○",10)
```

```python
def factorial(x):
     if x == 0:
         return 1
     else:
         return x * factorial(x - 1)
```

> 5  \*   factorial\(5 - 1\)  
>                                                    4 \* factorial\(4 - 1\)  
>                                                               3 \* factorial\(3 - 1\)  
>                                                                          2 \* factorial\( 2- 1\)  
>                                                                                      1 \*  factorial\( 1- 1\)  
>                                                                                                    1

```python
def factorial(x):
    return 1 if x==0 else x * factorial(x - 1)
```

## 2. 행결합/행분리

### - 행결합 : 세미콜론\(;\)

> 한행 여러 구문을 이어서 사용할때 쓴다

```python
# 세미콜론(semicolon) 사용법
print("Hello Python!!")
print("Hello Python!!");
print("첫번째 줄!!") print("두번째 줄") # 에러발생
print("첫번째 줄!!"); print("두번째 줄")
print("첫번째 줄!!"); print("두번째 줄");
```

### - 행분리 : \(\\)역슬래쉬 , 괄호  \(\)

> **1줄의 내용이 길어서 여러줄로 타이핑 해야 할경우 용**

```python
# 긴 내용을 한줄인것 처럼 인식 시키기(\ 사용)
a = 1 + 2 + 3 + \
      4 + 5 + 6
# 긴 내용을 한줄인것 처럼 인식 시키기(괄호 사용
b = (1 + 2 + 3 +
        4 + 5 + 6)
#  파라메터를 넘기는 것이라면 콤마(comma) 뒤에서 그냥 엔터를 쓰면 됩니다.
print("Hello",  "Python",
          end="\n", sep="\t")

# 문자열 중간에 줄바꿈을 하면 자동으로 ""가 열고닫히며 1줄로 인식한다.
print("아주 아주 아주 긴 문자열이라고 가정하자 " 
         "한줄에 모두 타이핑이 힘들다면")
```

## \*\* 파이썬이 제공하는 Turtle graphics 사용해보자 

{% code title="turtle\_ex1.py" %}
```python
# 거북이를 사용하기 위하여 라이브러리를 임포트
import turtle
# 일시정지한다.
turtle.done()
```
{% endcode %}

{% code title="turtle\_ex2.py" %}
```python
# 거북이를 사용하기 위하여 라이브러리를 임포트
import turtle
# 윈도우의 제목을 변경
turtle.title('거북')
# 거북이 색상을 변경
turtle.color('black','red')
# 거북이 출
turtle.shape('turtle')
# 클릭시 종료
turtle.exitonclick()
```
{% endcode %}

{% code title="turtle\_ex3.py" %}
```python
# 거북이를 사용하기 위하여 라이브러리를 임포트
import turtle
# 윈도우의 제목을 변경
turtle.title('거북')
# 거북이 색상을 변경
turtle.color('black','red')
# 거북이 출
turtle.shape('turtle')
 # 펜 준
turtle.penup()
 # 문자열 출력
turtle.write("거북아 놀자!!")
# 앞으로 80만큼 전
turtle.forward(80) 
# 펜 그리기 종
turtle.pendown() 
# 뒤로 100만큼 이동
turtle.backward(100) 
# 클릭시 종료
turtle.exitonclick()
```
{% endcode %}

* 앞으로 : forward\(이동거리\) 또는 fd\(이동거리\)
* 뒤로 : backward\(이동거리\) 또는 bk\(이동거리\) 또는 back\(이동거리\)
* 방향전환 : right\(각도\) 또는 rt\(각도\), left\(각도\) 또는 lt\(각도\)
* 그리기/이동하기 : penup\(\) 또는 pu\(\), pendown\(\) 또는 pd\(\)
* ※ 펜을 들고이동하면 이동하는 선이 그려지지않고 내리고 이동하면 선이 그려다.

{% hint style="danger" %}
다음과 나오도록 구문을 작성해보세요
{% endhint %}

![](../../../.gitbook/assets/image%20%2892%29.png)

## 

## 

