

### Question 

Given two cells on the standard chess board, determine whether they have the same color or not.

Example

For `cell1 = "A1"` and `cell2 = "C3"`, the output should be
solution(cell1, cell2) = true.


### Solution 

```python
def solution(cell1, cell2):
    c1 = (ord(cell1[0]) + int(cell1[1])) % 2
    c2 = (ord(cell2[0]) + int(cell2[1])) % 2
    return c1 == c2
```

## 
**give a star✨**
