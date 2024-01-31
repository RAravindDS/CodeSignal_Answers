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
def checking_index(vector_len, index_inside): 

  if index_inside == 0: 
    return list(range(index_inside, index_inside+2))

  elif index_inside == vector_len: 
    return list(range(index_inside-1, index_inside+1))

  else: 
    return list(range(index_inside-1, index_inside+2))
    


def solution(c): 

  c = [ list(map(int,i)) for i in c]
  length = len(c) - 1

  pura_list = []

  for index, vector in enumerate(c):
    temp_list = []
    index_inside = index

    for index_inside, element in enumerate(vector): 
      if index == 0:
        out = list(range(index, index+2)) 
        broo = checking_index(len(vector), index_inside)

        super_list = []
        for no_bro in out: 
          super_list.append(sum(c[no_bro][broo[0]:broo[-1]+1]))

        sum_of_super_list = sum(super_list) if vector[index_inside] == 0 else sum(super_list) - 1 
        temp_list.append(sum_of_super_list)
        


      elif index == length:
        out = list(range(index-1, index+1))
        broo = checking_index(len(vector), index_inside)

        super_list = []
        for no_bro in out: 
          super_list.append(sum(c[no_bro][broo[0]:broo[-1]+1]))
          
        sum_of_super_list = sum(super_list) if vector[index_inside] == 0 else sum(super_list) - 1 
        temp_list.append(sum_of_super_list)

      else:
        out = list(range(index-1, index+2))
        broo = checking_index(len(vector), index_inside)

        super_list = []
        for no_bro in out: 
          super_list.append(sum(c[no_bro][broo[0]:broo[-1]+1]))
          

        sum_of_super_list = sum(super_list) if vector[index_inside] == 0 else sum(super_list) - 1 
        temp_list.append(sum_of_super_list)

    pura_list.append(temp_list)

  return pura_list


```


**give a star ✨** 
