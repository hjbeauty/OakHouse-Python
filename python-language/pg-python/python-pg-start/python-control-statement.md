# control statement

## 1. 조건문 

{% hint style="info" %}
조건문이란  
: 조건\(상황\)에 따라 코드 실행/미실행 ==&gt; 어디로 갈까 결정
{% endhint %}

![](../../../.gitbook/assets/image%20%28121%29.png)

### - 조건문 공식1

![](../../../.gitbook/assets/image%20%286%29.png)

### - 조건문 공식2

![](../../../.gitbook/assets/image%20%2876%29.png)

{% tabs %}
{% tab title="실습 1" %}
```python
message = []

if message :
    print(message)
else:
    print("Empty")
```

```python
message2 = ["안녕"]

if message2 :
    print(message2)
else:
    print("Empty")
```

```python
money = 20000
card = 1

if money > 10000 or card :
    print("스타벅스 아메 먹자")
else:
    print("사무실 공짜 커피 먹자")
```

```python
bag = ["notebook",'손세정제','card']

if "money" in bag :
    print("별다방 가자 ")
else:
    print("사무실 가자")
```

```python
kim = 100
lee = 200

if kim >= lee :
    print(kim,"이", lee,"보다 크거나 같다")
else :
    print(kim,"이", lee,"보다 작다") 
```
{% endtab %}

{% tab title="실습 2" %}
```python
bag = ["notebook",'손세정제','card']
bus_card = 2

if "money" in bag :
    print("택시타고 가자 ")
elif bus_card:
    print("버스 타고 가자")
else :
    print("걸어서 가자")
```
{% endtab %}

{% tab title="실습 3" %}
![](../../../.gitbook/assets/image%20%28156%29.png)
{% endtab %}

{% tab title="실습 4" %}
```python
년도를 입력받아 윤/평년 판단
# 윤년 판단 규칙
# 1. 년도가 4로 나누어떨어지는 해는 윤년입니다. (1996년, 2004년, 2008년, 2012년 …)
# 2. 이 중에서 100으로 나누어떨어지는 해는 평년입니다. (1900년, 2100년, 2200년, 2300년 …)
# 3. 그중에 400으로 나누어떨어지는 해는 윤년입니다. (1600년, 2000년, 2400년 …)

while True:
    year = int(input('년도를 입력하시오(0은 종료)'))
    if not year:
        break

    # ver 1.0
    if not year%400:
        print('{}년은 "윤년"입니다.'.format(year))
    else:
        if not year%4:
            if year%100:
                print('{}년은 "윤년"입니다.'.format(year))
            else:
                print('{}년은 "평년"입니다.'.format(year))
        else:
            print('{}년은 "평년"입니다.'.format(year))

    # ver 1.5
    isLeapYear = False
    if not year%400:
        isLeapYear = True
    else:
        if not year%4:
            if year%100:
                isLeapYear = True
    print('{0}년은 "{1}년"입니다.'.format(year, '윤' if isLeapYear else '평'))

    # ver 2.0
    isLeapYear = year%400==0 or year%4==0 and year%100!=0
    print('{0}년은 "{1}년"입니다.'.format(year, '윤' if isLeapYear else '평'))

    # ver 3.0
    print('{0}년은 "{1}년"입니다.'
          .format(year, '윤' if year%400==0 or year%4==0 and year%100!=0 else '평'))
    
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="연습문제 1" %}
![](../../../.gitbook/assets/image%20%28149%29.png)
{% endtab %}

{% tab title="연습문제 2" %}
![](../../../.gitbook/assets/image%20%28179%29.png)

![](../../../.gitbook/assets/image%20%28168%29.png)
{% endtab %}

{% tab title="연습문제 3 " %}
![](../../../.gitbook/assets/image%20%2877%29.png)
{% endtab %}
{% endtabs %}

## 2. 반복문

{% hint style="info" %}
동일거나 규칙척으로 변화하는 작업이 조건에 맞는 동안 반복되면서 처리하는 문장 
{% endhint %}

### - 반복문 종

![](../../../.gitbook/assets/image%20%28204%29.png)

### -- while 

![](../../../.gitbook/assets/image%20%28197%29.png)

### -- while 문 실습 및 연습문

{% tabs %}
{% tab title="실습 1" %}
![](../../../.gitbook/assets/image%20%2879%29.png)
{% endtab %}

{% tab title="실습 2" %}
![](../../../.gitbook/assets/image%20%28122%29.png)
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="연습문제 1" %}
다음과 같은 결과가 나오도록 하세요

![](../../../.gitbook/assets/image%20%28155%29.png)

다음의 조건을 적절히 사용하여 만들어보

![](../../../.gitbook/assets/image%20%2854%29.png)
{% endtab %}

{% tab title="연습문제 2" %}
![](../../../.gitbook/assets/image%20%2873%29.png)
{% endtab %}
{% endtabs %}

## -- for ~ in ~~ 문 

![](../../../.gitbook/assets/image%20%28194%29.png)

![](../../../.gitbook/assets/image%20%28108%29.png)

## -- for in range

![](../../../.gitbook/assets/image%20%28128%29.png)

![](../../../.gitbook/assets/image%20%2886%29.png)



{% tabs %}
{% tab title="실습1" %}
```python
for k in 'abcdefghij' :
    print(k)

str =  'abcdefghij' 
for k in str :
    print(k)

```

```python
for k in [1,2,3,4,5] :
    print(k)

str = [1,2,3,4,5]
for k in str :
    print(k)
```
{% endtab %}

{% tab title="실습2" %}
```python
sum = 0
for i  in range(5) :
    sum += 1

print(sum)
```

```python
2 에서 10까지 짝수를 출력하는 방법
for i in range(2,12,2) :
    print(i)

for i in range(5) :
    print((i+1)*2)
```
{% endtab %}
{% endtabs %}

## break 

![](../../../.gitbook/assets/image%20%2856%29.png)

![](../../../.gitbook/assets/image%20%28157%29.png)

![](../../../.gitbook/assets/image%20%2842%29.png)











