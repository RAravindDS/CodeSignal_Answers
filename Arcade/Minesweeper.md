## Question 

In the popular Minesweeper game you have a board with some mines and those cells that don't contain a mine have a number in it that indicates the total number of mines in the neighboring cells. Starting off with some arrangement of mines we want to create a Minesweeper game setup.

Example

For
```
matrix = [[true, false, false],
          [false, true, false],
          [false, false, false]]
```

## answer 

```python
c = [[True, False, False, True], [False, False, True, False], [True, True, False, True], [False, True]]
# c = [[False, False, False], [False, False, False]]
c = [ list(map(int,i)) for i in c]
length = len(c) - 1



for index, vector in enumerate(c):
  temp_list = [] 

  if index == 0: 
    out = list(range(index, index+2))
    print(out)
    
    # for index_inside, element in  enumerate(vector):


  elif index == length: 
    out = list(range(index-1, index+1))
    print(out)


  else: 
    out = list(range(index-1, index+2))
    print(out)


```


**give a star ✨** 

(ongoing)
