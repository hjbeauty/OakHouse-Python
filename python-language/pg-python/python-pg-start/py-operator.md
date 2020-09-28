# Operator

## 연산자종류 

![](../../../.gitbook/assets/image%20%28120%29.png)

![](../../../.gitbook/assets/image%20%28110%29.png)

![](../../../.gitbook/assets/image%20%28185%29.png)

![](../../../.gitbook/assets/image%20%28152%29.png)

{% hint style="info" %}
연산자 정리 참조사이트

* [https://pydole.tistory.com/entry/Python-%EC%97%B0%EC%82%B0%EC%9E%90Operator%EC%9D%98-%EC%A2%85%EB%A5%98](https://pydole.tistory.com/entry/Python-%EC%97%B0%EC%82%B0%EC%9E%90Operator%EC%9D%98-%EC%A2%85%EB%A5%98)
* [https://docs.python.org/3/library/operator.html?highlight=operator](https://docs.python.org/3/library/operator.html?highlight=operator)
{% endhint %}

## 1. 산술 연산자 \(+, - , \*, / , \*\* , //, %\) [https://docs.python.org/3/library/operator.html?highlight=operator](https://docs.python.org/3/library/operator.html?highlight=operator)

```python
print(3 + 4)
print(3 - 4)
print(3 * 4)
print(3 / 4)
```

* 누 : \*\*
* 정수 몫 : //
* 정수 나머지 : % 

```python
print(12 / 7)
print(12 // 7)
print(12 % 7)
print(12 ** 7)
```

### - 문자열 

* 이중따옴표 또는 싱글따옴표로 표시한 
* 파이썬은 문자라는 자료형은 존재하지 않는다 모두 문자열이다

```python
어디서 에러가 날까요? 이유는?
print ( 3 + 5)
print ( '3' + 5)
print ( '3' + '5')
print ( '3 + 5')
print ( '3' + "5")
print ( '3" + "5')

```

```python
결과?
print('Hello World!!')
print("Hello World!!")
print("나의 이름은 '김말자'입니다.")
print('나의 이름은 "김말자"입니다.')
print("나의 이름은 \"김말자\"입니다.")
print('나의 이름은 \'김말자\'입니다.')
```

{% hint style="danger" %}
우리의 비대면 수업은 'Webex'로 합니다   를 출력해보자
{% endhint %}

> ### 문자열 앞 0으로 채우기 zfill\(\)

```python
#  앞의 빈칸 0으로 채우기
값을 예측하시고 자바에는?
print('12'.zfill(5))
print('-12'.zfill(5))
print('3.141'.zfill(7))
print('-3.141'.zfill(7))
print('3.14159265359'.zfill(5))
print('-3.14159265359'.zfill(5))
print('문자열'.zfill(10))
print('문자열'.zfill(1))
```

> ### 길이와 정렬
>
> * {:길이} : 출력할 데이터의 길이를 지정. 문자열\(왼쪽 정렬\), 숫자\(오른쪽 정렬\)
> * {:&lt;길이} : 왼쪽 정렬
> * {:&gt;길이} : 오른쪽 정렬
> * {:^길이} : 가운데 정렬

```python
예
print('Python is [{:15}]'.format('good'))
print('Python is [{:<15}]'.format('good'))
print('Python is [{:>15}]'.format('good'))
print('Python is [{:^15}]'.format('good'))
print('당신의 나이는 [{:15}]세'.format(22))
print('당신의 나이는 [{:<15}]세'.format(22))
print('당신의 나이는 [{:>15}]세'.format(22))
print('당신의 나이는 [{:<15}]세'.format(22))
```

### - 문자열 연산   

* 연결 : +
* 반복 : \*

```python
print("베니 " + "밤비")
print("베니 " , "밤비")
print("베니♥" * 7)
```

{% hint style="danger" %}
연산자를 이용하여 수를 분리하여 보세요

1. 96,000원 은 5만원 : 1장 , 1만원 : 4장, 5천원: 1장, 1천원 : 1장 이 필요
2. birth = 20030222 ,  생년월일 : 2003년 2월 22일
{% endhint %}

## 2. 관계 연산자 \(Relational Operators\)

{% hint style="info" %}
#### 관계 연산자 <a id="1-relational-operators"></a>

 **&gt; : 크다**  
**&gt;= : 크거나 같다**  
**&lt; : 작다**  
**&lt;= : 작거나 같다**  
**== : 같다**  
**!= : 같지 않다**
{% endhint %}

## 3. 논리 연산자\(Logical Operators\)

{% hint style="info" %}
#### 논리 연산자\(Logical Operators\)

 **and : 논리곱**  
**or : 논리합**  
**not : 논리부정**
{% endhint %}

{% hint style="danger" %}
다음 문제를 풀어보세요

1. **1~10사이의 수중에서 3의 배수 또는 5의 배수 출력**
2. **1~10사이의 3의 배수만 빼고 출력**
3. **년도를 입력받아 윤년 판단하기**
{% endhint %}

## 4. 삼항 연산자\(Ternary operators\)

{% hint style="info" %}
 **참인경우 값 if 조건 else 거짓인경우 값**

print\("짝수" if num % 2 == 0 else "홀수"\)  
~println\(\(num %  2\)==0 ? "짝수" : "홀수"\); 
{% endhint %}

{% hint style="danger" %}
음 문제를 풀어보세요

1. **년도와 월을 입력받아 월을 마지막 날짜 구하기**
2. **년도를 입력받아 윤년 판단하기**
{% endhint %}

## 5.  멤버 연산자\(Membership Operators\)

{% hint style="info" %}
#### 멤버 연산자\(Membership Operators\) <a id="1-membership-operators"></a>

1.  **in 연산자** : 포함하는지 검사.
2. **not in 연산자** : 포함되어 있지 않은지 검사 .
{% endhint %}

![](../../../.gitbook/assets/image%20%28145%29.png)

## 6. 아이디 연산자\(Identity Operators\)

{% hint style="info" %}
#### 아이디 연산자\(Identity Operators\) <a id="1-identity-operators"></a>

> **is** : 양쪽 Operand가 동일한 Object를 가리키는지 아닌지 검사  
> **is not** : 양쪽 Operand가 다른 Object를 가리키는지 아닌지 검사.

* 동일한 객체 여부를 판별하는 연산자
* id\(\) 함수는 객체를 입력값으로 받아서 객체의 고유값\(레퍼런스\)을 반환하는 함수.
* id는 파이썬이 객체를 구별하기 위해서 부여하는 일련번호. 숫자로서 의미는 없다.
* id는 동일한 객체 여부를 판별할 때 사용.
{% endhint %}

![](../../../.gitbook/assets/image%20%28123%29.png)

## 7. 연산 우선 순위\(Operators Precedence\) 

![](../../../.gitbook/assets/image%20%28213%29.png)

