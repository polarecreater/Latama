
**Split 함수**
- String 타입의 값을 나눠서 list형태로 변환됨


```python
items = 'crazy sexy cool'.split()
```


```python
print(items)
```

    ['crazy', 'sexy', 'cool']
    


```python
items = 'crazy~sexy~cool'.split('~')
print(items)
```

    ['crazy', 'sexy', 'cool']
    


```python
# 변수에 넣기 - unpacking
item = 'homeWhomeWhomeWhome'
a,b,c,d = items.split('W')
```


```python
print(a,b,c,d)
```

    home home home home
    

**Join 함수**
- String List를 합쳐서 하나의 String으로 반환


```python
result = '~'.join(items)
print(result)
```

    crazy~sexy~cool
    


```python

```
