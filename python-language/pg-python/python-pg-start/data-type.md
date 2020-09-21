# Data Type

![](../../../.gitbook/assets/image%20%2821%29.png)

## 1. 수치자료형

{% hint style="info" %}
## Numbers type

1. **정수형**

* 양의 정수, 0, 음의 정수, 소수이하 값이 없는 자료형
* 비트 수에 의해 제한되지 않고 사용 가능한 메모리의 한계까지 확장 될 수 있다 . 따라서 큰 수를 저장하기위한 특별한 배열을 필요로하지 않다

2. 실수형

* 실수형\(Floating\)은 소수점이 포함된 숫자.
* 부동 소수점 숫자는 소수점 이하 15 자리까지.
* 정수 및 부동 소수점은 소수점으로 구분됩니다. 1정수, 1.0부동 소수점 숫자다.

3. 복소수형

* x + yj 처럼 복소수 형태로 쓰여집니다. i가 아니라 j입니다.
* x 는 실수 부분이고 y 는 허수 부분입니다.
* 실수부와 허수부를 따로 분리가 가능합니다.
* 복소수끼리의 연산도 지원 합니다.
{% endhint %}

```text
number1 = 127
number2 = 127.89
complex_number1 = 1.2 + 3.4j
```

![](../../../.gitbook/assets/image%20%2814%29.png)

{% hint style="danger" %}
다음 결과는?
{% endhint %}

![](../../../.gitbook/assets/image%20%28115%29.png)

## 2. String

### -- 문자열 생성 

![](../../../.gitbook/assets/image%20%28171%29.png)

![](../../../.gitbook/assets/image%20%28126%29.png)

![](../../../.gitbook/assets/image%20%28166%29.png)

![](../../../.gitbook/assets/image%20%28199%29.png)

![](../../../.gitbook/assets/image%20%2823%29.png)

![](../../../.gitbook/assets/image%20%2889%29.png)

{% hint style="info" %}
**문자열 잘라내기**

> **문자열\[n:m\]**  
> \[n\] : 1글자 잘라내기  
> \[n:m\] : n부터 m-1까지 문자열을 리턴.  
> \[:m\] : 앞의 숫자를 생략하면 0부터 시작.  
> \[n:\] : 뒤의 숫자를 생략하면 끝 글자까지린턴.  
> \[:\] : 모두 생략하면 전체리.  
> \[-n\] : 음수 값을 지정하면 뒤에서부터 카운팅.
{% endhint %}

{% hint style="info" %}
**앞뒤 공백없애기**

> **문자열.strip\(\) , 문자열.lstrip\(\), 문자열.rstrip**  
> strip\(\) : 앞, 뒤 공백을 모두 없앤다.  
> lstrip\(\) : 왼쪽 공백을 없앤다.  
> rstrip\(\) : 오른쪽 공백을 없앤다.
{% endhint %}

{% hint style="info" %}
**문자 개수세기**

> **문자열.count\(문자열\)**  
> 문자열에서 지정 문자열의 개수를 세어 다.
{% endhint %}

{% hint style="info" %}
**대, 소문자 바꾸기**

> **문자열.upper\(\), 문자열.lower\(\)**  
> 문자열을 대문자 또는 소문자로 바꿔다.
{% endhint %}

{% hint style="info" %}
**문자열 찾기**

> **문자열.find\(문자열\)**  
> **문자열.index\(문자열\)**  
> 두개의 차이점은 find\(\)는 없으면 -1을 리턴하고 index\(\)는 에러를 발생.
{% endhint %}

{% hint style="info" %}
**문자열 바꾸기**

> **문자열.replace\('원본문자열', '바뀔문자열',개수=None\)**

※  문자열은 불변객체입니다.  
자신이 변경되는것이 아니라 항상 새로운 객체를 만들어 리턴, 변경을 하려고하면 다음과 같이 에러를 발생합니다.  
TypeError: 'str' object does not support item assignment
{% endhint %}

{% hint style="info" %}
**문자열 나누기, 합치기**

> **문자열 나누기 : 문자열.split\(self, sep=None, maxsplit=-1\)**  
> **문자열 합치기 : 문자열.join\(self, iterable\)**
{% endhint %}

{% hint style="info" %}
**간단한 변환함수**

> ord : 문자의 아스키 코드값을 리턴하는 함수  
> hex : hex\(x\)는 정수값을 입력받아 16진수\(hexadecimal\)로 변환하여 리턴하는 함수  
> otc : oct\(x\)는 정수 형태의 숫자를 8진수 문자열로 바꾸어 리턴하는 함수  
> chr : 아스키\(ASCII\) 코드값을 입력으로 받아 그 코드에 해당하는 문자를 리턴하는 함수  
> capitalize : 단어의 첫글자만 대문자로 변환하는 함수
{% endhint %}

{% hint style="danger" %}
다음 결과는?
{% endhint %}

![](../../../.gitbook/assets/image%20%2861%29.png)

## 3. Bool

![](../../../.gitbook/assets/image%20%28109%29.png)

## 3. List 

{% hint style="info" %}
list

* list는 자료들의 모음
* 순서 유지
* list\(\)생성자나 \[ \]로 리스트를 만듬.
* set과 다르게 1개짜리 리스트도 만들 수 있.
* 어떤 자료 형도 저장이 가능.
{% endhint %}

![](../../../.gitbook/assets/image%20%2891%29.png)

![](../../../.gitbook/assets/image%20%2837%29.png)

![](../../../.gitbook/assets/image%20%28195%29.png)

![](../../../.gitbook/assets/image%20%289%29.png)

{% hint style="info" %}
#### 리스트의 길이, 추가, 삽입, 수정, <a id="2"></a>

* len\(\)  .
* \[n:m\] 
* append\(\) 
* insert\(\) 
* remove\(\)
* clear\(\) 
{% endhint %}

{% hint style="info" %}
#### 정렬, 뒤집기, 복사 <a id="3"></a>

* reverse\(\)
* sort\(\) 
* sorted\(\) 
* copy\(\)
{% endhint %}

## 4. Tuple

{% hint style="info" %}
#### tuple <a id="1-tuple"></a>

* tuple 자료형은 데이터의 목록 
* 콤마\(,\)로 데이터를 나열하면 tuple
* 괄호\(\)안에 ,로 나열해도 tuple
* 길이 1개짜리 tuple을 만들려면 반드시 뒤에 콤마\(,\)를 붙여야 한
* tuple은 다른 자료형들로 만들 수 있다.
* tuple은 tuple을 가질 수 있다
* **tuple은 불변 객체**
  * tuple의 요소 값 변경이 불가합니다.
  * tuple의 요소 삭제가 불가합니다.
{% endhint %}

![](../../../.gitbook/assets/image%20%28221%29.png)

![](../../../.gitbook/assets/image%20%28105%29.png)

{% hint style="info" %}
####  tuple에 접근하기 <a id="2-tuple"></a>

* **len\(tuple\)**로 요소의 개수를 알아낼 수 있다.
* **\[n:m\]**으로 요소에 접근이 가능. 사용법은 문자열과 동일
* 반복문을 이용하여 접근이 가능.
* **+연산**을 이용하여 결합이 가능.
* **\*연산**을 이용하여 반복할 수 있다.
{% endhint %}

## 5. Dictionary

{% hint style="info" %}
####  dictionary\(사전\)  <a id="1-dictionary"></a>

* dictionary는 "키\(Key\)/값\(Value\)" 쌍을 요소로 갖는 자료형.
* dictionary는 흔히 Map 이라고도 불다. 키\(Key\)로 신속하게 값\(Value\)을 찾아내는 해시테이블\(Hash Table\) 구조를 갖다
* "dict" 클래스로 구현되어 있다.
* dictionary의 키\(key\)는 그 값을 변경할 수 없는 Immutable 타입이어야 하며, dictionary 값\(value\)은 Immutable과 Mutable 모두 가능. 예를 들어, dictionary의 키\(key\)로 문자열이나 Tuple은 사용될 수 있는 반면, 리스트는 키로 사용될 수 없다.
* dictionary의 요소들은 {} 를 사용하여 만다. 여러개일 경우 콤마\(,\)로 구분
* {}를 이용하여 만들 수 있
* dict\(\) 생성자를 이용하여 만들 수 있다.
{% endhint %}

![](../../../.gitbook/assets/image%20%2833%29.png)

![](../../../.gitbook/assets/image%20%2832%29.png)

{% hint style="info" %}
#### dictionary 조작하기 <a id="2-dictionary"></a>

* keys\(\) 
* values\(\) 
* "dict객체\[키\]=값"
* update\(\)
* "del dict객체\[키\]"
* items\(\) 메서드로 \(key,value\)쌍 얻을 수 있다.
{% endhint %}

## 6. Set

{% hint style="info" %}
#### set이란? <a id="1-set"></a>

* set 자료형은 중복을 허용하지 않다.
* set은 입력된 순서는 중요하지 않다.
* set\(\) 생성자 함수를 이용해서 만들 수 있다.
* {}를 이용해서 만들 수 있다.
* add\(\) 메서드를 이용하여 추가가 가능.
* update\(\) 메서드를 이용하여 동시에 여러개 추가가 가능.
* remove\(\) 메서드를 이용하여 삭제가 가능.
* copy\(\) 메서드를 이용하여 복사가 가능.
* clear\(\) 메서드를 이용하여 모든 요소 삭제가 가능
{% endhint %}

![](../../../.gitbook/assets/image%20%28176%29.png)

## 7. Range

![](../../../.gitbook/assets/image%20%28203%29.png)

