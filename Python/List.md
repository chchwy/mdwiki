# List

list 是數據的線性集合, 用方括號包起來[]就可以建立 list

    fruit = ['Apple', 'Banana', 'Orange']
    
使用 `len()` 來得知 list 元素的個數

    len(fruit)    => 3
    
使用方括號來索引任意位置元素

    fruit[0]      => Apple
    fruit[1]      => Banana
    
也可以用負號數, -1就是最尾端的元素

    fruit[-1]     => Orange
    
超出索引範圍會丟出 IndexError

    fruit[5]      => IndexError
    

用 `append()` 可以往尾端添加元素

    fruit.append( 'Lime' )   => ['Apple','Banana','Orange','Lime']
    
用 `insert()` 在指定位置插入元素

```python
fruit.insert(1, 'Pineapple')
>>> ['Apple','Pineapple','Banana','Orange','Lime']
```

用 `pop()` 來刪除尾端元素

```python
fruit.pop()
>>> ['Apple','Pineapple','Banana','Orange']
```

pop() 也可以指定 index, 刪除指定位置的元素

```python
fruit.pop(2)
>>> ['Apple','Pineapple','Orange']
```