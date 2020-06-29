```python

MAX_VALUE=2**31-1

MIN_VALUE=-2**31

class Solution:

  def reverse(self, x: int) -> int:

​    \# num=str(x)

​    \# result=""

​    \# if num[0]=="-":

​    \#   for i in range(len(num)-1,0,-1):

​    \#     result+=num[i]

​    \#   rnum=int("-"+result)

​    \#   if rnum<MIN_VALUE :

​    \#     return 0

​    \#   else:

​    \#     return rnum

​    \# else :

​    \#   for i in range(len(num)-1,-1,-1):

​    \#     result+=num[i]

​    \#   rnum=int(result)

​    \#   if rnum>MAX_VALUE:

​    \#     return 0

​    \#   else :

​    \#     return rnum

​    rev=0

​    tmp=abs(x)

​    while tmp!=0:

​      rev=rev*10+tmp%10

​      tmp=int(tmp/10)

​    if (x>0 and rev>MAX_VALUE) or (x<0 and (-rev)<MIN_VALUE):

​      return 0

​    elif x>0:

​      return rev

​    else :

​      return -rev