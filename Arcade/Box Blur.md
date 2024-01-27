
## Question 
Last night you partied a little too hard. Now there's a black and white photo of you that's about to go viral! You can't let this ruin your reputation, so you want to apply the box blur algorithm to the photo to hide its content.

The pixels in the input image are represented as integers. The algorithm distorts the input image in the following way: Every pixel x in the output image has a value equal to the average value of the pixel values from the 3 × 3 square that has its center at x, including x itself. All the pixels on the border of x are then removed.
Return the blurred image as an integer, with the fractions rounded down.

Example

For
```python 
image = [[1, 1, 1], 
         [1, 7, 1], 
         [1, 1, 1]]
```
the output should be solution(image) = [[1]].

## Answer: 

```python
import numpy as np 


def solution(a): 

  bro = np.array(a)

  brs = []
  count = 0
  outer_count = 0
  second_loop = 0

  for i in range(len(a)-2):
    intermediate_list = []

    for bros in range(len(a[0])-2): 
      intermediate_list.append(int(bro[outer_count:3+second_loop, count:3+count].mean()))
      count += 1
    
    brs.append(intermediate_list)
    second_loop += 1 
    outer_count += 1
    count = 0 

  return brs
```

**Give a star ✨**
