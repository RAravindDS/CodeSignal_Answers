

### Questions 
Check if all digits of the given integer are even.

Example

For n = 248622, the output should be
solution(n) = true;
For n = 642386, the output should be
solution(n) = false.

##

### answer: 
```python 
def solution(a):
    return len(str(a)) == len(list(filter(lambda x: x if int(x) %2 == 0 else "", str(a))))
```


## 
**give a star✨**
