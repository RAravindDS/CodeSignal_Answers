
### Question 
Consider integer numbers from 0 to n - 1 written down along the circle in such a way that the distance between any two neighboring numbers is equal (note that 0 and n - 1 are neighboring, too).

Given n and firstNumber, find the number which is written in the radially opposite position to firstNumber.

Example

For n = 10 and firstNumber = 2, the output should be
solution(n, firstNumber) = 7.

##

### Answer 
```python 
def solution(num, target):
    y=target
    for i in range(1,num):
        x=target+i
        if(y!=0):
            y=y-1
        else:
            y=num-1
        if(x>=num):
            x=x-num
        if(x==y):
            return x

## created by shukla
```

**give a star✨**
