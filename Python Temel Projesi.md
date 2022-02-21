# Python Temel Proje


#### Soru-1

Bir listeyi düzleştiren (flatten) fonksiyon yazın. Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak:

input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

output: [1,'a','cat',2,3,'dog',4,5]


```python
y = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]
sonuclist = []
    
def flatten(x):
    for i in x:
        if type(i)==list:
            flatten(i)
        else:
            sonuclist.append(i)

flat(y)
print(sonuclist)

```

    [1, 'a', 'cat', 2, 3, 'dog', 4, 5]
    

#### Soru-2

Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. Örnek olarak:

input: [[1, 2], [3, 4], [5, 6, 7]]

output: [[[7, 6, 5], [4, 3], [2, 1]]


```python
y = [[1, 2], [3, 4], [5, 6, 7]]
sonuclist = []

def ters(x):
    for i in x:
        if type(i)==list:
            sonuclist.append(list(reversed(i)))
            
            
        

ters(y)
print(list(reversed(sonuclist)))
```

    [[7, 6, 5], [4, 3], [2, 1]]
    
