# 차원에 의한 명칭

### 0차원\(Scalar\) a = 4

* numpy array : 1 또는 5, 10와 같이 숫자 데이터
* array\(\)
* shape\(\) : 머신러닝에서 행렬의 차원을 표현
* Scalar는 shape,행렬차원이 아무것도 없는 것 

```text
arr_scalar = np.array(10)
arr_scalar
```

```text
arr_scalar.shape
```

### 1차원\(Vector\) a = \[3,4\]

* 리스트 \[\]로 데이터를 씌우게 되면 차원이 생긴다
* 열의 연속
* shape를 표현 할 때 \(1\)이 아닌\(1, \) 출력
* \(3, \) : 1차원에 3개의 값\(value\)이 들어가있다 

```text
arr_vector = np.array([10,3])
print(arr_vector)
```

```text
arr_vector.shape
```

```text
arr_vector = np.array([1, 2, 3])
print(arr_vector)
arr_vector.shape
```



### 2차원\(Matrix\) a = \[ \[ 3\] , \[4\] \]

* \[ \[ \] \] : vector \[ \]에 대괄호를 한 번 더 씌우면 차원이 추가적 생김
* shape 의 결과가 \(3,2\) : 3행,2열 3X2

```text
arr = np.array([[10]])
print(arr)
arr.shape
```

```text
arr_matrix1 = np.array([[1,  3], [4, 6], [7, 9]])
print(arr_matrix1)
arr_matrix1.shape
```

```text
test_array = [[1,2,3,4],[1,2,3,4]]
arr_matrix2 = np.array(test_array)
print(arr_matrix2)
arr_matrix2.shape
```



### 다 차원\(Tensor\) a = \[ \[ \[ 3\] ,\[4\]\], \[\[5\],\[6\] \] \]

* 3 차원이상

```text
arr_tensor = np.array([[[1, 2,1,2], [4, 5,4,5], [8, 9,8,9]], [[1, 2,1,2], [4, 5,4,5], [7, 8,7,8]]])
print(arr_tensor)
arr_tensor.shape
```

```text
arr_tensor2 = np.array([[[[1, 2, 3,1], [4, 5, 6,1], [7, 8, 9,1]],
                         [[1, 2, 3,1], [4, 5, 6,1], [7, 8, 9,1]]], 
                        [[[1, 2, 3,1], [4, 5, 6,1], [7, 8, 9,1]], 
                        [[1, 2, 3,1], [4, 5, 6,1], [7, 8, 9,1]]]])
print(arr_tensor2)
arr_tensor2.shape
```



### 차원 변경

* reshape : 만들어진 행력을 다른 차원으로 변경
  * -1  : size를 기반으로 row 개수를 선정하는 옵션입니다. 
* flatten : 배열을 1차원 형태의 배열로 변환

```text
arr_vector = 
print(arr_vector)
print(arr_vector.shape)

arr_vector_reshape = arr_vector.reshape(2,1)
print(arr_vector_reshape)
print(arr_vector_reshape.shape)

[10  3]
(2,)
[[10]
 [ 3]]
(2, 1)
```

```text
test_array = 
arr_matrix2 = np.array(test_array)
print(arr_matrix2)
arr_matrix2.shape

[[1 2 3 4]
 [1 2 3 4]]
(2, 4)
```

```text
arr_matrix2_reshape2 =  
print(arr_matrix2_reshape2)
print(arr_matrix2_reshape2.shape)

[[1 2]
 [3 4]
 [1 2]
 [3 4]]
(4, 2)
```

```text
arr_matrix2_reshape =  
print(arr_matrix2_reshape)
print(arr_matrix2_reshape.shape)

[1 2 3 4 1 2 3 4]
(8,)
```



* flatten 

```text
arr_matrix2_flatten = 
print(arr_matrix2_flatten)
print(arr_matrix2_flatten.shape)

[1 2 3 4 1 2 3 4]
(8,)
```

