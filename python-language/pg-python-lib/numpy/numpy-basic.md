# Numpy Basic

#### [Data Types](https://numpy.org/doc/stable/reference/arrays.scalars.html)

* Boolean
* Integer
* Unsigned Integer
* Float
* Complex
* String  
  * 부호가 있는 정수 int\(8, 16, 32, 64\)
  * 부호가 없는 정수 uint\(8 ,16, 32, 54\)
  * 실수 float\(16, 32, 64, 128\)
  * 복소수 complex\(64, 128, 256\)
  * 불리언 bool
  * 문자열 string\_
  * 파이썬 오프젝트 object
  * 유니코드 unicode\_

출처: [https://doorbw.tistory.com/171](https://doorbw.tistory.com/171) \[Tigercow.Door\] ==&gt; 데이타 형태 지정하기\(assigning Data type\)  
 : dtype = np.Type   
 ==&gt; 데이타 형태 확인하기\(checking Data type\)  
 : object.dtype  
 ==&gt; 데이타 형태 변환하기\(converting Data type\)  
 : object.astype\(np.Type\)

```text
import numpy as np
```

* dtype : array의 data type 확인 

```text
arr = np.array([[1, 2, 3], [1, 2, 3]])
arr.dtype
arr = np.array([[1., 2, 3], [1, 2, 3]])
arr.dtype
```

* astype\(\) : datatype 변환 가능

```text
arr = arr.astype(np.int32)
arr
```

```text
arr = np.array([[-1.6, 2, 3], [1, 2, 3]], dtype=np.uint8)
arr.dtype
```



* len\(arr.shape\) : 차원의 갯수,  
* ndim : 차원 수를 return 

```text
arr.shape

len(arr.shape)


```

* size 확인

```text
arr.size
```



* dtype 확인

```text
arr.dtype
```

### Reshape

```text
arr.shape
```

Reshape

```text
arr =  
print(arr)
arr =  
print(arr)
print(arr.shape)
print(arr.size)

[1 2 6 4 8 3]
[[1]
 [2]
 [6]
 [4]
 [8]
 [3]]
(6, 1)
6
```

```text
arr =  
print(arr)
print(arr.size)

[[1 2 3]
 [1 2 3]]
6
```

```text
arr.reshape([6])
```

Reshape, -1 활용

```text
arr =  
print(arr)
arr.shape

[1 2 3 1 2 3]
(6,)
```

```text
arr = arr.reshape(   )
print(arr)
arr.shape

[[1 2 3]
 [1 2 3]]
(2, 3)
```

random array 생성

