# TwoSum
Given an array of integers, return indices of the two numbers such that they add up to a specific target.

Example: 

`Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
`

You may assume that each input would have exactly one solution. Also, you should assume there are no duplicated entries in the array.

# How to Solve It?
1. Think about the total number of solutions: use the brute force solution, do 2 round iterations. For any number in the array, iterator the rest numbers to find its complement. This leads to a O(N^2) solution.
2. Then think about how to optimize it. In the brute force solution, it scans the whole array to find its complement. Can we find the complement in O(1) complexcity? Which data structure can find an element it O(1)? Obviously, it's a map. Therefore, we first iterate to build a map. That leads to the 2-pass hash map solution.
3. Can it be further optimized? That's 1-pass hash map solution. As we build the map, we check if the complement is in the map. When the second element of the result is being checked, the first element must be in the map.

# Common Pitfalls
1. Sort the array first: If sorting the array, you will not get the original indeices.
2. 2-pass hash map solution: when checking if the complement is in the map, should exclude the current index. For example, [3, 2, 4], targe = 6, [0, 0] is the wrong solution.
3. 1-pass hash map solution: the lower index shoud come first.
