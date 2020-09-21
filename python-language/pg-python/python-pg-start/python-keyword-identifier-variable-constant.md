# 키워드, 식별자, 변수, 상수, 리터럴

## 1. Keyword

### 파이썬 예약어\(자바와비숫\)

![](../../../.gitbook/assets/image%20%28100%29.png)

![](../../../.gitbook/assets/image%20%28165%29.png)

![](../../../.gitbook/assets/image%20%2831%29.png)

#### Built-in Constants\(예약어 이면서 내장상수 \)

* 파이썬에서 미리 만들어 놓은 상수 대표적으로  논리값True, False,  값이 없음None 등  , 자바에서 true , false , null

![](../../../.gitbook/assets/image%20%2813%29.png)

![](../../../.gitbook/assets/image%20%28187%29.png)

## 2. [식별자\(identifier\)](http://www.ktword.co.kr/abbr_view.php?m_temp1=5775)

#### 요소 간에 구별/식별성을 주는 이름 또는 표식 또는 숫자

```text
 ㅇ 프로그램 안에서 식별자는,
     - 구성요소 간에 구별/식별성을 주는 이름 (주로, 프로그래머가 정하는 이름)
        . 例) 변수명,상수명,레이블명,함수명,메소드명,클래스명,타입명 등 

  ㅇ 한편, 프로그래밍 언어에서는, 미리 정의되는 언어 구성자 로써, 크게 두가지로 구분 가능
     - 재정의 불가능 식별자 : 예약어 라고 함
     - 재정의 가능 식별자   : 미리 정의되었지만, 재정의가 가능한 식별자

  ※ [참고] 
     - 식별자/예약어/키워드/토큰 등의 비교 ☞ 식별자 예약어 키워드 토큰 어휘항목 비교 참조
     - 식별자 이름 충돌 방지 ☞ 네임스페이스 참조
     http://www.ktword.co.kr/abbr_view.php?m_temp1=5775
```

{% hint style="info" %}
### S[tyle Guide for Python Code](https://www.python.org/dev/peps/pep-0008/%20)[ https://www.python.org/dev/peps/pep-0008/ ](%20https://www.python.org/dev/peps/pep-0008/%20)

**코딩 규칙\(배치\)**

* 들여쓰기는 공백 4칸을 권장
* 한 줄은 최대 79자까지
* 최상위\(top-level\) 함수와 클래스 정의는 2줄씩 띄어 쓴
* 클래스 내의 메소드 정의는 1줄씩 띄어 쓴

**구문의 공백을 피하는곳**

* 대괄호\(\[\]\)와 소괄호\(\(\)\)안의 공백

  쉼표\(,\), 쌍점\(:\)과 쌍반점\(;\) 앞의 공백

* 키워드 인자\(keyword argument\)와 인자의 기본값\(default parameter value\)의 = 는 붙여 다.

**주석**

* 코드와 모순되는 주석은 없앤
* 불필요한 주석은 달지 않는
* 한 줄 주석은 신중히
* 문서화 문자열\(Docstring\)에 대한 컨벤션은 PEP 257을 참고.

**이름 명명 규칙**

* 변수명에서 \_\(밑줄\)은 위치에 따라 다음과 같은 의미가 있다.
  * 1개의 밑줄로 시작 : 내부적으로 사용되는 변수
  * 1개의 밑줄로 종료 : 파이썬 기본 키워드와 충돌을 피하려고 사용
  * 2개의 밑줄로 시작 : 클래스 속성으로 사용
  * 2개의 밑줄로 종료 : 사용자가 조정할 수 있는 네임스페이스 안의 속성
* 소문자 L, 대문자 O, 대문자 I는 변수명으로 사용하지 말
* 모듈\(Module\) 명은 짧은 소문자로 구성되며 필요하다면 밑줄로 나눈니다.
* 클래스명은 카멜케이스\(CamelCase\)로 작성
  * 내부적으로 쓰이면 밑줄을 앞에 붙인다.
  * 예외\(Exception\)는 실제로 에러인 경우엔 “Error”를 뒤에 붙다.
* 함수명은 소문자로 구성하되 필요하면 밑줄로 나다.
* 메소드명은 함수명과 같으나 비공개\(non-public\) 메소드, 혹은 변수면 밑줄을 앞에 붙다.
* 서브 클래스\(sub-class\)의 이름 충돌을 막기 위해서는 밑줄 2개를 앞에 붙다.
* 상수\(Constant\)는 모듈 단위에서만 정의하며 모두 대문자로 표.

**프로그래밍 권장 사항**

* None을 비교할때는 is나 is not만 사용.
* 클래스 기반의 예외를 사용
* 모듈이나 패키지에 자기 도메인에 특화된\(domain-specific\)한 기반 예외 클래스\(base exception class\)를 빌트인\(built-in\)된 예외를 서브클래싱해 정의하는게 좋습니다. 이 때 클래스는 항상 문서화 문자열\("""~"""\)을 포함해야 합니다.
* 예외를 except:로 잡기보단 명확히 예외를 명시.\(ex. except ImportError:
* try: 블록의 코드는 필요한 것만 최소한으로 작성
* string 모듈보다는 string 메소드 사용. 메소드는 모듈보다 더 빠르고, 유니코드 문자열에 대해 같은 API를 공유다.
* 접두사나 접미사를 검사할 때는 startswith\(\)와 endwith\(\)를 사용.
* 객체의 타입을 비교할 때는 isinstance\(\)를 사용
* 빈 시퀀스\(문자열, 리스트\(list\), 튜플\(tuple\)\)는 조건문에서 거짓\(false\)다.
* 불린형\(boolean\)의 값을 조건문에서 ==를 통해 비교하지 말.
{% endhint %}

{% hint style="info" %}
###  식별자 작성 규칙\(자바와거의일\)

* 식별자는 소문자 \(a ~ z\) 또는 대문자 \(A ~ Z\) 또는 숫자 \(0 ~ 9\) 또는 밑줄 \(\_\)의 조합
* myClass, var\_1및 print\_this\_to\_screen 모두 사용가
* 식별자는 숫자로 시작될 수 없다. 1variable 불가능 variable1 가
* 키워드는, !, @, \#, $, % 등 특수 기호는 불가.
* 식별자의 길이는 제한이 없다.
* 파이썬은 대소 문자를 구별
* 의미있는 식별자로 명
{% endhint %}

## 3. 변수 \(variable\)

### - 변수란 

* 정보 보관소\(메모리 공간\)

![](../../../.gitbook/assets/image%20%28192%29.png)

![](../../../.gitbook/assets/image%20%2852%29.png)

![](../../../.gitbook/assets/image%20%2850%29.png)

{% hint style="danger" %}
 다음 결과를 예측하세요
{% endhint %}

![&#xC608;&#xCE21;1](../../../.gitbook/assets/image%20%2895%29.png)

![&#xC608;&#xCE21;2](../../../.gitbook/assets/image%20%28106%29.png)

![&#xC608;&#xCE21;3](../../../.gitbook/assets/image%20%28101%29.png)

![&#xC608;&#xCE21;4](../../../.gitbook/assets/image%20%2866%29.png)

### - 변수명 \(virable name\)

* 변를 대신하여 사용할 이름으로 신중하게 만들어야 한다

#### -- 변수명 만드는 규

![](../../../.gitbook/assets/image%20%28224%29.png)

{% hint style="danger" %}
변수와 연산자를 사용하여 다음의 문제를 풀어보세
{% endhint %}

![](../../../.gitbook/assets/image%20%28169%29.png)

#### -- 특별한 변수 지정

* 중복 지정  :  a = b = c =10
* 동시 지정 :  a, b = 1, 2

![](../../../.gitbook/assets/image%20%28119%29.png)

## 4. 상수\(constant\)

상수\(constant\)는 항상 똑같은 값을 저장하고 있는 곳, 프로그래머나 시스템에 의해 미리 정해져있는 것으로, 복잡한 숫자의 값을 인지하기 쉬운 문자로 변경하여 사용

{% tabs %}
{% tab title="myconstant.py" %}
```python
PI = 3.141592
```
{% endtab %}

{% tab title="use\_constant.py" %}
```python
import myconstant

print(myconstant.PI)

myconstant.PI = 3.14 # 에러가 나지 않는다 
print(myconstant.PI)
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="myconstant.py" %}
```python
class _myconstant:
    def __setattr__(self, name, value):
        if name in self.__dict__:
            raise Exception('변수에 값을 할당할 수 없습니다.')
        self.__dict__[name] = value

    def __delattr__(self, name):
        if name in self.__dict__:
            raise Exception('변수를 삭제할 수 없습니다.')

import sys
sys.modules[__name__] = _myconstant()
```
{% endtab %}

{% tab title="use\_constant.py" %}
```python
import myconstant

myconstant.PI = 3.141592
myconstant.MAX = 1000
print(myconstant.PI)
print(myconstant.MAX)

myconstant.PI = 3.14
myconstant.MAX = 2000
print(myconstant.PI)
print(myconstant.MAX)
```
{% endtab %}
{% endtabs %}

{% hint style="danger" %}
에러가 날까요? 어디서  날까요?   
{% endhint %}

## 3. 리터럴\(Liternal\)

* 리터럴\(liternal\)은 "값" 그 자체로, 고정된 값을 표현하는 것을 의미

**-- 수치리터럴 종** 

* 정수 리터럴 : 0b로 시작하면 2진수, 0o로 시작하면 8진수 ,0~9로 시작하면 10진수, 0x로 시작하면 16진수
* 실수 리터럴 : 소숫점을 포함하거나 e를 포함
* 복소수 리터럴 : j로 끝나면 복소수의 허수를 나타낸

![](../../../.gitbook/assets/image%20%2844%29.png)

{% hint style="danger" %}
 실행결과를 예측해보세
{% endhint %}

#### -- 문자 리터

따옴표로 묶이는 데이

"r"문자는 raw string으로 백슬래시 문자를 해석하지 않고 남겨두기 때문에 정규표현식과 같은 곳에 유용

![](../../../.gitbook/assets/image%20%28207%29.png)



