# TwoSum
Given an array of integers, return indices of the two numbers such that they add up to a specific target.

Example: 

`Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
`

You may assume that each input would have exactly one solution. Also, you should assume there are no duplicated entries in the array.

# Frenquent Wrong Solutions

1. Sort the array first:
If sorting the array, you will not get the original indeices.
2. 2-pass hash map solution: when checking if the complement is in the map, should exclude the current index. For example, [3, 2, 4], targe = 6, [0, 0] is the wrong solution.
3. 1-pass hash map solution: the lower index shoud come first.