

### Question 
Correct variable names consist only of English letters, digits and underscores and they can't start with a digit.

Check if the given string is a correct variable name.

Example

For name = "var_1__Int", the output should be

solution(name) = true;

For name = "qq-q", the output should be

solution(name) = false;

For name = "2w2", the output should be

solution(name) = false.
##
### Answer 
```python 
import re 

def solution(name):
    expression = r"^[a-zA-Z_][a-zA-Z0-9_]*"
    return len(name) == len("".join(re.findall(expression, name)))
```


##
**give a star✨**
