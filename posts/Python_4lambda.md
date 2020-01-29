

```python
f = lambda x, y: x + y
print(f(1,4))
```

    5
    

**Lambda**
- 함수 이름 없이, 함수처럼 쓸 수 있는 익명함수
- 수학의 람다 대수에서 유래
- Python 3 부터는 권장하지 않으나 여전히 많이 쓰임


```python
f = lambda x: x ** 2
print(f(3))
```

    9
    


```python
f = lambda x: x/2
print(f(3))
```

    1.5
    


```python
print((lambda x: x+1)(5))
```

    6
    

**Map function**
- Sequence 자료형 각 element에 동일한 function을 적용함


```python
ex = [1,2,3,4,5]
f = lambda x:x ** 2
print(list(map(f,ex)))#list를 꼭 붙여야 값이 나옴
```

    [1, 4, 9, 16, 25]
    


```python
f = lambda x, y : x+y
print(list(map(f, ex, ex)))#1+1=2, 2+2=4... 순서대로 더해짐 -> zip함수와 같은 효과
```

    [2, 4, 6, 8, 10]
    


```python
list(map(
    lambda x: x ** 2 if x%2 == 0 else x,  #조건을 만족하지 않을 때 else값을 꼭 넣어줘야 함
    ex))
```




    [1, 4, 3, 16, 5]



*람다 함수 안 써도 리스트 컴프리헨션으로 사용 가능*


```python
[value ** 2 for value in ex]
```




    [1, 4, 9, 16, 25]



*리스트를 사용하지 않아 for문을 사용한다면..*


```python
f = lambda x: x**2
print(map(f,ex)) #리스트를 사용하지 않아 주소가 찍힘
for i in map(f, ex):
    print(i)
```

    <map object at 0x000002CAA8DE6588>
    1
    4
    9
    16
    25
    

**Reduce function**
- list에 똑같은 함수를 적용해서 통합시킴
- map과 reduce는 같이 사용하는 경우가 많음
- 판다스를 사용할 때 reduce를 유용하게 사용


```python
from functools import reduce
print (reduce(lambda x, y: x+ y, [1,2,3,4,5]))#1+2=3, 3+3=6...
```

    15
    


```python
def factorial(n):
    return reduce(
        lambda x, y: x*y, range(1,n+1))
```


```python
factorial(5)
```




    120




```python

```
