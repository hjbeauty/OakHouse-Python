# Standard Input/Output

## 0. Console Input Output 을 위한 명령

* Console : Keyboard , Monitor등 입력이 가능한 device 

{% hint style="info" %}
입/출력 매체에 따른 Application

* Console, command 창 : 가장 기본이 되는 콘솔어플리케이션
* 윈도우모드 : Window Application, Desktop Application 예\) 이클립스등
* 스마트기기 : App 예\)카카오톡등
* 웹브라우저 : web application 예\) 쿠팡사이트등
{% endhint %}

## 1. 표준출력   print\( \)

{% hint style="info" %}
[http://helloworldcollection.de/](http://helloworldcollection.de/)
{% endhint %}

```python
# Hello world in Python 2
print "Hello World"

# Hello world in Python 3
print("Hello World")
```

{% hint style="warning" %}
파이썬2x ,3x 버전설명 :   [https://wiki.python.org/moin/Python2orPython3](https://wiki.python.org/moin/Python2orPython3) 
{% endhint %}

```python
# print함수의 도움말을 확인해 보자
help(print)

print (7)
print("김말자")
print('김말자')
```

{% hint style="danger" %}
일주일은 몇 초인지 print\(\) 를 사용해서 출력해보세요
{% endhint %}

```python
print("하나","둘","셋",1,2,3) 
print("하나","둘","셋",1,2,3,sep='-') 
print("첫번째 값")
print("두번째 값") 
print("첫번째 값", end=" ---> ")
print("두번째 값") 
# 출력 방향 변경
file = open("test.txt","w")
print("Hello Python!!", file=file) # 파일로 출력
file.close()
```

{% hint style="danger" %}
결과를 예측하세요
{% endhint %}

{% hint style="info" %}
 확장문자 **escape sequence** 

* \' : 따옴표 문자
* \" : 쌍따옴표 문자 
* \ : backslash 문자 
* \a : bell 문자 
* \b : backslash 문자 
* \f : Formfeed 문자
* \n : newline 문자
* \r : carriage return 문자\(\n와 동일하지 않다.\) 
* \t : tab 문자 
* \v : vertical tab 문자
{% endhint %}

```python
print('Hello \tWorld!!')
print("Hello \nWorld!!")
print("나의 이름은 \"김말자\"입니다.")
print('나의 이름은 \'김말자\'입니다.')
print('-' * 40)
print('1 \n')
print('2 \012')
print('3 \x0A')
print('-' * 40)
print('n')
print('\156')
print('\x6E')
print('-' * 40)
```

{% hint style="info" %}
### {}와 % 출력

* {}를 출력하려면 "{"과 "}"을 세번 연달아 입력해야 한다.
* % 자체를 출력하려면 %%로 입력해야 다.
{% endhint %}

```python
print('{0}씨는 상위 {1}%안에 있는 사람입니다.'.format('김말자',10))
print('{{0}}씨는 상위 {{1}}%안에 있는 사람입니다.'.format('김말자',10))
print('{{{0}}}씨는 상위 {{{1}}}%안에 있는 사람입니다.'.format('김말자',10))
print('%s씨는 상위 %d%%안에 있는 사람입니다.'%('김말',10))
```

{% hint style="info" %}
### 형식에 format 맞추어 출력 : "출력형식".format\(데이터...\)

* "{}" 지정하면 format에 기술한 출력 대상들이 대응되어 출력.
* "{n}"안에 숫자를 지정하여 출력 대상의 위치를 지정
* 함수의 인자처럼 키워드를 사용해서 나타낼 수 있다
* 동일한 데이터를 여러번 출력할 수 있다.
{% endhint %}

```python
# 파이썬(Python) 3 포맷팅 방식
print('나의 이름은 {}입니다'.format('김말자'))
print('나의 이름은 "{0}"입니다. 나이는 {1}세이고 성별은 {2}입니다.'.format('김말',33,'남성'))
print('나이는 {1}세이고 성별은 {2}입니다. 나의 이름은 "{0}"입니다. '.format('김말자',33,'남성'))
print('나이는 {age}세이고 성별은 {gender}입니다. 나의 이름은 "{name}"입니다. '
         .format(name='김말자',age=33,gender='남성'))
print('만세삼창 :  {0}!!! {0}!!! {0}!!! '.format('만세'))
print('삼삼칠 박수 :  {0}!!! {0}!!! {1}!!! '.format('짝'*3,'짝'*7))
print('-' * 40)
```

{% hint style="danger" %}
위 문장의 결과와 동일한 자바 문장을 적어보세
{% endhint %}

{% hint style="info" %}
### 채움문자와 숫자 표시형식

* [ ] { \[ 인덱스 \] : \[ 채움문자 \] \[ 정렬 \] \[ 길이 \] \[ , \| \_ \] \[ 형식문자 \]   }
* {        1        :          ★             &gt;          5                        d               }
  * print\("@{1:★&gt;5d}@".format\(7,9,2\)\)
  * 결과 ==&gt; @★★★★9@
{% endhint %}

![](../../../.gitbook/assets/image%20%28129%29.png)

{% hint style="danger" %}
### 코드와 결과를 확인한후 채움과 정렬에 대한 규칙을 찾아보세요
{% endhint %}

## 2. 표준 입력 Input\(\)

```python
# 도움말을 통해 input의 사용방법 확인
help(input)
```

{% hint style="info" %}
input\(\)

* input\(\) : console로 입력받은 데이터를 문자열로 리턴
* input\('문자열'\) : 문자열을 출력하고 console로 부터 데이터를 입력 받고 문자열을  리턴
* 사용자가 EOF \(Linux: Ctrl-D, Windows: Ctrl-Z+Return\)을 입력하면 EOFError를 발생시킨다
{% endhint %}

![input\(\) vs input\(&apos;ddd&apos;\)](../../../.gitbook/assets/image%20%28136%29.png)

![567 =&amp;gt; str??](../../../.gitbook/assets/image%20%28164%29.png)

{% hint style="info" %}
### int 입력

* eval\(인자\) 함수 : 인자를 유효한 파이썬 표현식으로 리턴
* int\(\) 클래스 : class int\(x=0\), class int\(x,base=10\)                        숫자나 문자열 x 로 부터 만들어진 정수 객체를 리턴                       인자가 주어지지 않으면 0 을 리턴                       base는 2, 8, 10, 16진법,  10이 디폴트.
{% endhint %}

![&amp;lt;str &#xC5D0; int &#xC744; +&#xC5F0;&#xC0B0;&#xD560; &#xC218; &#xC5C6;&#xB2E4;&amp;gt;](../../../.gitbook/assets/image%20%28205%29.png)

![eval\(\) vs int\(\)](../../../.gitbook/assets/image%20%2848%29.png)

![](../../../.gitbook/assets/image%20%28196%29.png)

{% hint style="info" %}
### float 입력

* eval\(인자\) 함수 : 인자를 유효한 파이썬 표현식으로 리턴
* float\(\) 클래스 : class float\(x\) 숫자나 문자열 x 로 부터  실수 객체를 린턴, 인자가 주어지지 않으면 0 .0을 리턴 .
{% endhint %}

![](../../../.gitbook/assets/image%20%28182%29.png)

![](../../../.gitbook/assets/image%20%28102%29.png)

{% hint style="info" %}
### collection 입력
{% endhint %}

![](../../../.gitbook/assets/image%20%28153%29.png)



