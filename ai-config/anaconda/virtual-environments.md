---
description: '프로젝트를 만들기 위한  workspace와 같은 것 ,  eclipse =프로젝트'
---

# Virtual Environments\(가상환경\)

> eclipse -&gt; .java 를 만들려해도 우선 프로젝트단위로 작업합니다.  
>                    java version, jdk 의 위치 설정 , jdbc  lib ,  하나씩 lib폴더에  ~~.jar lib 파일,  
>   
> A=--,P-- , V---  : 가상환경 , 프로젝트단위로 작업 을 하기 위한 ,~~

## \* PIP 설치   

1. 팩케이지를 설치할수 있는 툴 -  **pip**는 [파이썬](https://ko.wikipedia.org/wiki/%ED%8C%8C%EC%9D%B4%EC%8D%AC)으로 작성된 패키지 소프트웨어를 설치 · 관리하는 패키지 관리 시스템이다.    pip 최신버전으로 update부터! 관리자권한으로 아나콘다 프롬프트 실행 **python -m pip install --upgrade pip**

![](../../.gitbook/assets/image%20%28134%29.png)

## \* 가상환경 설치

1. 우리가 작업할 가상공간 생성! python 최신말고 3.7으로, 추가적으로 openssl은 먼저 설치하는 것이 좋음\( **OpenSSL**은 [네트워크](https://ko.wikipedia.org/wiki/%EC%BB%B4%ED%93%A8%ED%84%B0_%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC)를 통한 데이터 통신에 쓰이는 [프로토콜](https://ko.wikipedia.org/wiki/%ED%94%84%EB%A1%9C%ED%86%A0%EC%BD%9C)인 [TLS](https://ko.wikipedia.org/wiki/%ED%8A%B8%EB%9E%9C%EC%8A%A4%ED%8F%AC%ED%8A%B8_%EB%A0%88%EC%9D%B4%EC%96%B4_%EB%B3%B4%EC%95%88)와 [SSL](https://ko.wikipedia.org/wiki/SSL)의 [오픈 소스](https://ko.wikipedia.org/wiki/%EC%98%A4%ED%94%88_%EC%86%8C%EC%8A%A4) 구현판이다. [C 언어](https://ko.wikipedia.org/wiki/C_%EC%96%B8%EC%96%B4)로 작성되어 있는 중심 라이브러리 안에는, 기본적인 암호화 기능 및 여러 유틸리티 함수들이 구현되어 있다.\)  
   machine learning에 사용할 windows용 TensorFlow 는 1.15버전을 사용\(현재 버전은 2.x\) 그에 맞추어 사용할 파이썬 버전은 3.7버전을 이용. 

   **==&gt; conda  create  -n**  _**가상공간폴더**_  **python=3.7  openssl**   

          **conda  create  -n**   _**data\_env**_          **python=3.7  openssl**

```
(base) C:\Windows\system32>conda create -n data_env  python=3.7   openssl
```

![](../../.gitbook/assets/image%20%2880%29.png)

![](../../.gitbook/assets/image%20%28143%29.png)

![](../../.gitbook/assets/image%20%2863%29.png)

## \* 생성된 가상환경 확인 및 전환

1. 정상적으로 됬는지 확인

   conda info --envs

2. 사용할 가상환경으로 이동해보자

   1. activate   가상공간이름
   2. activate data\_env

           \(base\) C:\Users\USER&gt;activate data\_env

           \(data\_env\) C:\Users\USER&gt;

