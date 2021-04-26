# numpy

> **NumPy는 Numerical Python의 약자로 배열 또는 다양한 자료구조를 다룰 수 있는 클래스들을 포함하고 있는 패키지**
>
> List를 사용한 배열
>
> * 다수의 List를 이용해 다차원의 배열을 쉽게 생성
> * 다차원 배열은 다수의 List를 하나로 묶은 배열

```text
flot_list = [1.0, 10.4, 3.2, 5.1, 7.5, 2.7] # 변수 np에 실수 list 생성
flot_v =  
flot_v

[[1.0, 10.4, 3.2, 5.1, 7.5, 2.7], [1.0, 10.4, 3.2, 5.1, 7.5, 2.7]]
```

* 1차원 배열 값 추출

> flot\_v는 다차원 배열  
>  flot\_v\[n\]을 이용해 n차원 배열 값 출력

```text



[1.0, 10.4, 3.2, 5.1, 7.5, 2.7]
```

* 1차원 배열의 요소에 다른 값 대입

> flot\_v\[n\]=다른값 , 다차원배열

```text
flot_v[0]=
flot_v

['Python', [1.0, 10.4, 3.2, 5.1, 7.5, 2.7]]
```

#### NumPy 사용해봅시다

numpy install

**&gt; !pip install numpy  ==&gt; colab**

**&gt; pip install numpy  ==&gt; pycharm 의 terminal**

**&gt; import numpy as np**

```text
import numpy as np 
```

**np.array함수를 사용한 값을 변수 a에 저장**

```text
a = [1,2,3]
print(   )
a = np.array(a) # a = np.array([1,2,3])
print(       )  # numpy 배열의 유형은 numpy.ndarray


<class 'list'>
<class 'numpy.ndarray'>
```

```text
isinstance(a,     ) # a가 numpy의 array의 인스턴스 인지 확인 

True
```

```text
np.ndarray(a) 
np.array(a) 
```

```text
a = np.array([1, 2.5, 4.0, 5.5, 7.0])



[1.  2.5 4.  5.5 7. ]
[5.5 7. ]

```

