# make-bricks-Python
We want to make a row of bricks that is goal inches long. We have a number of small bricks (1 inch each) and big bricks (5 inches each). Return True if it is possible to make the goal by choosing from the given bricks. This is a little harder than it looks and can be done without any loops.


``` python
def make_bricks(small, big, goal):
  b = int(goal/5)
  s = int(goal/1)
  b1 = min(b,big)
  p = goal%5
  if small*1==goal or big*5==goal:
    return True
  elif small*1+big*5==goal:
    return True
  elif min((goal-(b1*5)),small)==(goal-(b1*5)):
    return True
  else:
    return False
    
```



sample cases:

![image](https://user-images.githubusercontent.com/87606741/213912211-a754d0d5-5616-474c-992c-a4bbcbc9d726.png)
