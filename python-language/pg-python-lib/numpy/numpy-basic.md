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
arr =  [1 2 6 4 8 3]
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



### zeros & ones

* zeros : 0으로 채워진 numpy array를 만들 수 있음
* ones : 1으로 채워진 numpy array를 만들 수 있음

```text
arr_zeros=np.array([[0,0,0],[0,0,0],[0,0,0]])
print(arr_zeros) 
```

```text
arr_zeros = np.zeros([3, 3],dtype=np.int32)
print(arr_zeros)
```

```text
arr_zeros = np.zeros(1)
print(arr_zeros)
```

```text
arr_ones = np.ones([10])
print(arr_ones)
```

```text
arr_ones * 5
```



* arange : 연속적인 값을 갖는 1차원 배열을 만듬

```text
arr = np.arange(9).reshape(3, 3)
arr
```



## Index

* 배열에 대한 indexing
* arr\[r,c\]
* arr\[r\]\[c\]

```text
arr = np.arange(9).reshape(3, 3)
arr
arr[1][2]
arr[1, 2]
```



## Slicing

* arr\[s:e\] : s~ e-1
* arr\[s1:e1, s2:e2\] : s1~ e1-1,s2~ e2-1

```text
arr[1:, 1:]
```

### Boolean Indexing

```text
ran_data = np.random.randn(3, 3)
ran_data

ran_data <= 0
```



## Broadcast '흩뿌리고 퍼뜨리고 전파'

* broadcast는 Numpy 배열에서 차원의 크기가 서로 다른 배열에서도 산술 연산을 가능하게 하는 원리

  **- 규칙**

* 차원\(ndim\)이 낮은 배열이 차원이 높은 배열로 인식.
* 반환된 배열은 연산을 수행한 배열 중 차원의 수\(ndim\)가 가장 큰 배열이 된다.
* 연산에 사용된 배열과 반환된 배열의 차원의 크기\(shape\)가 같거나 1일 경우 브로드캐스팅이 가능
* 브로드캐스팅이 적용된 배열의 차원 크기\(shape\)는 연산에 사용된 배열들의 차원의 크기에 대한 최소 공배수 값으로 사용
* 형식 캐스팅\(type casting\)을 지원해 두 배열의 자료형\(dtype\)이 다르더라도 연산이 가능

```text
array1 = np.array([1, 2, 3, 4]).reshape(2, 2)
print(array1)
print(array1.shape,"  , " ,array1.ndim)
```

```text
array2 = np.array([1.5, 2.5])
print(array2)
print(array2.shape,"  , " ,array2.ndim)
```

```text
add_res = array1 + array2
print(add_res)
print(add_res.shape,"  , " ,add_res.ndim)
```

```text
arr = np.arange(9).reshape(3, 3)
arr
```

```text
arr_brodcasting= arr + np.array([1, 2, 3])
arr_brodcasting
```



### 차원축소 연산\(dimension reduction\)

* 최대/최소: min, max, argmin, argmax
* 통계: sum, mean, median, std, var
* 불리언: all, any



numpy , [axis](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcSoMOs%2Fbtqt0a2Dc2y%2FQhkfwhiWqeUKvNfsM2H29K%2Fimg.png) 개념

* axis = 0 : 행방향
* axis = 1 : 열방향
* axis = 2 : 면\(대각선\) 축방향 



