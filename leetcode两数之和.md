```python

class Solution:

  def twoSum(self, nums: List[int], target: int) -> List[int]:

​    \# for i in range(0,len(nums)):

​    \#   for j in range(i+1,len(nums)):

​    \#     if (nums[i]+nums[j])==target:

​    \#       return [i,j]

​    \# for i in range(0,len(nums)):

​    \#   if target-nums[i] in nums[i+1:len(nums)]:

​    \#     j=nums[i+1:len(nums)].index(target-nums[i])

​    \#     return [i,j+i+1]

​    numd={}

​    for i in range(0,len(nums)):

​      num=target-nums[i]

​      if num in numd.keys():

​        return [numd.get(num),i]

​      numd[nums[i]]=i