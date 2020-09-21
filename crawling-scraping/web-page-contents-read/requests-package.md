# requests package

{% hint style="info" %}
## requests 패키지

* Kenneth Reitz에 의해 개발된 파이썬 라이브러리 HTTP 프로토콜과 관련된 기능 지원
* &lt; [https://2.python-requests.org/en/master/](https://2.python-requests.org/en/master/) &gt;
{% endhint %}

{% hint style="danger" %}
## pipenv install requests

* 아나콘다에는 requests 패키지가 site-packages로 설치되어 있음 만일 설치를 해야 한다면 pipenv 명령으로 설치
{% endhint %}

![](../../.gitbook/assets/image%20%28232%29.png)

## requests.request\(\)

![](../../.gitbook/assets/image%20%28231%29.png)

## requests.models.Response 처리 ...

> requests.request\(\), requests.get\(\), requests.head\(\), requests.post\(\) 함수 모두 리턴 값은 requests.models.Response

{% hint style="info" %}
### text

* 문자열 형식으로 응답 콘텐츠 추출 - 추출 시 사용되는 문자 셋은'ISO-8859-1’==&gt; 'utf-8’이나  'euc-kr' 문자 셋으로 작성된 콘텐츠  추출 시 한글이 깨지는 현상 발생
* 추출 전 응답되는 콘텐츠의 문자 셋  정보를 파악하여 Response 객체의  encoding 속성에 문자 셋 정보를  설정한 후 추출
{% endhint %}

{% hint style="info" %}
## content

* 바이트열 형식으로 응답 콘텐츠 추출 
* 응답 콘텐츠가 이미지와 같은 바이너리 형식인 경우 사용 
* 한글이 들어간 문자열 형식인 경우 r.content.decode\('utf-8'\)를 사용해서 디코드 해야 함
{% endhint %}

```python
#ex1
import requests
from bs4 import BeautifulSoup
import re

req = requests.get('http://movie.naver.com/movie/point/af/list.nhn?page=1')
1
2
print(soup)

3
4
5
movie_title = []
movie_point = []
movie_review = [] 

for dom in titles:
6

for dom in points:
7

for dom in reviews:
8

commentLength = len(movie_title)   

for i in range(commentLength):
    print("영화 제목 : " + movie_title[i])
    print("평점 : " + movie_point[i])
    print("리뷰글 : " + movie_review[i])
    print("-----------------------------------------")

```

