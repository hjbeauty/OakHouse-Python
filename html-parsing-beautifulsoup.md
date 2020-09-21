# HTML parsing - BeautifulSoup

{% hint style="success" %}
## BeautifulSoup

* HTML 및 XML 파일에서 데이터를 추출하기 위한 파이썬 라이브러리
* **pip install beautifulsoup4**
* pip install lxml

  pip install html5lib
{% endhint %}

## HTML 파싱

* BeautifulSoup의 메인 패키지인 bs 패키지에서 BeautifulSoup\(\) 함수 임포트
* 파싱할 HTML 문서와 파싱에 사용할 파서\(구문 분석기\)를 지정하여 호출
* HTML 문서에 대한 파싱이 끝나면 트리 구조 형식으로 DOM 객체 생성from bs4 import BeautifulSoup

  bs = BeautifulSoup\(html\_doc, 'html.parser'\)

  bs = BeautifulSoup\(html\_doc, 'lxml'\)

  bs = BeautifulSoup\(html\_doc, 'lxml-xml'\)  bs = BeautifulSoup\(html\_doc, 'html5lib'\)

![Parser Library](.gitbook/assets/image%20%28241%29.png)

### bs4.BeautifulSoup 객체의 태그 접근 방법

![](.gitbook/assets/image%20%28225%29.png)

![](.gitbook/assets/image%20%28239%29.png)

