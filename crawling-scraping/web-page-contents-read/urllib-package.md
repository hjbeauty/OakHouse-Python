# urllib package

{% hint style="info" %}
## urllib

* 파이썬의 표준 라이브러리 URL 작업을 위한 여러 모듈을 모은 패키지
{% endhint %}

{% hint style="info" %}
### URL 문자열과 웹 요청에 관련된 모듈

* urllib.request : URL 접속 요청 기능  
* urllib.response : 응답 클래스들 
* urllib.parse :  파싱하여 해석하는 기능 
* urllib.error : urllib.request에 의해 발생하는 예외 처리 클래스
* urllib.robotparser : robots.txt 파일을 구문 분석하는 기능 제공
{% endhint %}

## urllib.request 모듈

* URL 문자열을 가지고 HTTP 요청을 수행
* urlopen\(\) 함수를 사용하여 웹 서버에 페이지를 요청
* 서버로부터 받은 응답을 저장하여 응답 객체\(http.client.HTTPResponse\) 반환

## http.client.HTTPResponse 클래스

* 웹 서버로부터 받은 응답을 래핑하는 객체 응답 
* 헤더나 응답 바디의 내용을 추출하는 메서드 제공

### http.client.HTTPResponse - read\(\) 메서드 

###  웹 서버가 전달한 데이터\(응답 바디\)를 바이트열로 읽어 들임

{% hint style="info" %}
#### 바이트열

* 16진수로 이루어진 수열이기 때문에 읽기 어려우므로 웹 서버가 보낸 한글을 포함한 텍스트 형식의 HTML 문서의 내용을 읽을 때는 텍스트 형식으로 변환함
* 바이트열\(bytes\)의 decode\(‘문자 셋’\) 메서드를 실행하여 응답된 문자 셋에 알맞은 문자로 변환함
{% endhint %}

![](../../.gitbook/assets/image%20%28236%29.png)

{% hint style="success" %}
#### 웹 페이지 인코딩 체크

* &lt;meta charset="utf-8"&gt;
* encode = f.info\(\).get\_content\_charset\(\)
{% endhint %}

![](../../.gitbook/assets/image%20%28228%29.png)

![](../../.gitbook/assets/image%20%28237%29.png)

## 

## urllib.parse

* 웹 서버에 페이지 또는 정보를 요청할 때 함께 전달하는 데이터
* 영문과 숫자는 그대로 전달되지만 한글은 %기호와 함께 16진수 코드 값으로 전달되어야 함
* 웹 크롤링을 할 때 요구되는 Query 문자열을  함께 전달해야 하는 경우, 직접 Query 문자열을  구성해서 전달해야 함

{% hint style="info" %}
### urllib.parse.urlparse\("URL문자열"\)

* URL 문자열의 정보를 파싱하고 각각의 정보를 정해진 속성으로 저장하여 urllib.parse.ParseResult 객체를 리턴
{% endhint %}

![](../../.gitbook/assets/image%20%28243%29.png)

{% hint style="info" %}
### urllib.parse.urlencode\(\)

* 메서드의 아규먼트로 지정된 name과 value로 구성된 딕셔너리 정보를 정해진 규격의 Query 문자열 또는 요청 파라미터 문자열로 리턴
{% endhint %}

![](../../.gitbook/assets/image%20%28234%29.png)

![](../../.gitbook/assets/image%20%28227%29.png)























