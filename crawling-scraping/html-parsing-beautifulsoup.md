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

![Parser Library](../.gitbook/assets/image%20%28271%29.png)

### bs4.BeautifulSoup 객체의 태그 접근 방법

![](../.gitbook/assets/image%20%28229%29.png)

![](../.gitbook/assets/image%20%28268%29.png)

![](../.gitbook/assets/image%20%28261%29.png)

![](../.gitbook/assets/image%20%28269%29.png)

![](../.gitbook/assets/image%20%28263%29.png)

![](../.gitbook/assets/image%20%28274%29.png)

![](../.gitbook/assets/image%20%28228%29.png)

> * •BeautifulSoup : HTML 및 XML 파일에서 데이터를 추출하기  위한 파이썬 라이브러리
> * BeautifulSoup\(\) 함수 호출 시 HTML 문서에 대한 파싱이  끝나면 트리 구조 형식으로 DOM 객체들이 생성되며  bs4.BeautifulSoup 객체를 통해 접근 가능
> * &lt;html&gt;, &lt;head&gt; 태그와 &lt;body&gt; 태그는 제외하고 접근하려는  태그에 대하여
>
>   계층 구조를 적용하여 태그명을 . 연산자와 함께 사용
>
> * 태그명은 bs4.element.Tag 객체의 name 속성, 태그의 속성은  bs4.element.Tag 객체에 \['속성명'\] 식을 적용하고 태그의  내용은 bs4.element.Tag 객체의 text 속성 사용
> * bs4.BeautifulSoup 객체의 find\_all\(\)은 주어진 기준에 맞는 모든 태그들을 찾아오며 결과는 bs4.element.ResultSet 객체로 리턴
> *  bs4.BeautifulSoup 객체의 bs.find\(\)는 주어진 기준에 맞는 태그 한 개를 찾아오며 결과는 bs4.element.Tag 객체로 리턴하며 결과값이 없으면 None을 리턴 
> * bs4.BeautifulSoup 객체의 bs.select\(\) 주어진 CSS 선택자에 맞는 모든 태그들을 찾아오며 결과는 list 객체로 리턴

