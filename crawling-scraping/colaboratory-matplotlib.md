# Colaboratory Matplotlib 에서 한글폰트 사용하기



## Colaboratory Matplotlib 에서 한글폰트 사용하기

### 참고

* 링크: [https://programmers.co.kr/learn/courses/21/lessons/950](https://programmers.co.kr/learn/courses/21/lessons/950)
* 총 3가지 방법 중에서 실제 사용할만하다 싶은 하나만 해봄

```text
%matplotlib inline  

import matplotlib as mpl  # 기본 설정 만지는 용도
import matplotlib.pyplot as plt  # 그래프 그리는 용도
import matplotlib.font_manager as fm  # 폰트 관련 용도

```

## 한글 깨지는 것 확인하기

```text
# 데이터 준비
import numpy as np

data = np.random.randint(-200, 100, 50).cumsum()
data
```

```text
# 한글을 넣어놓고 그러보면 깨진다
plt.figure(figsize=(10,8))
plt.plot(range(50), data, 'r')
plt.title('시간별 가격추이')
plt.ylabel('주식가격')
plt.xlabel('시간(분)')
```

## 버전과 위치정보를 알아두자

* 이후 필요하게 될 수 있다. 

```text
print(mpl.__version__)
print(mpl.__file__)
print(mpl.get_configdir())
print(mpl.get_cachedir())
```

## 시스템에 설치된 폰트 확인. 나눔은 없다

```text
sys_font=fm.findSystemFonts()
print(f"sys_font number: {len(sys_font)}")
print(sys_font)

nanum_font = [f for f in sys_font if 'Nanum' in f]
print(f"nanum_font number: {len(nanum_font)}")
```

## 나눔글꼴  설정, 확인

```text
path = '/usr/share/fonts/truetype/nanum/NanumGothicEco.ttf'  # 설치된 나눔글꼴중 원하는 글꼴의 전체 경로
font_name = fm.FontProperties(fname=path, size=10).get_name()
print(font_name)
plt.rc('font', family=font_name)
```

```text
plt.plot(range(50), data, 'r')
plt.title('시간별 가격 추이')
plt.ylabel('주식 가격')
plt.xlabel('시간(분)')
plt.style.use('seaborn-pastel')
plt.show()
```

### 안된다 ==&gt; 다음을 해주고 

### fm.\_rebuild\(\)

fm.\_rebuild\(\) 를 해줘야 system 에 추가 설치된 폰트를 matplotilb.font\_manager 가 알아차리는 것으로 보인다. [https://pinkwink.kr/1255](https://pinkwink.kr/1255)

```text
# fm._rebuild() 를 해주고 , 런타임 초기화 해준다
fm._rebuild()
# 다시 그려보자
plt.plot(range(50), data, 'r')
plt.title('시간별 가격 추이')
plt.ylabel('주식 가격')
plt.xlabel('시간(분)')
plt.style.use('seaborn-pastel')
plt.show()
```

![](../.gitbook/assets/image%20%28306%29.png)

그래도 안나오면 메뉴에서 런타임--&gt;런타임다시시

