
### Question 

Given a string, your task is to replace each of its characters by the next one in the English alphabet; i.e. replace a with b, replace b with c, etc (z would be replaced by a).


For inputString = `"crazy"`, the output should be solution(inputString) = `"dsbaz"`.

### Answer 
```python
def solution(inputString):
    return "".join([chr(ord(i)+1) if i != "z" else chr(ord(i)-25) for i in list(inputString)])
```


##
**give a star✨**
