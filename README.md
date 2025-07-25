# Leetcode-1534.-Count-Good-Triplets

# Description
Given an array of integers arr, and three integers a, b and c. You need to find the number of good triplets.

A triplet (arr[i], arr[j], arr[k]) is good if the following conditions are true:

0 <= i < j < k < arr.length
|arr[i] - arr[j]| <= a
|arr[j] - arr[k]| <= b
|arr[i] - arr[k]| <= c
Where |x| denotes the absolute value of x.

Return the number of good triplets.
# Solution
We need to find the number of triplets in the array which satisfies the 3 conditions:

|arr[i] - arr[j]| <= a

|arr[j] - arr[k]| <= b

|arr[i] - arr[k]| <= c

Example:

Input: arr = [3,0,1,1,9,7], a = 7, b = 2, c = 3

(3,0,1) 

3-0 < 7 

0-1 < 2

3-1 < 3 

In a similar way we have more such pairs which satisfies the condition :

[(3,0,1), (3,0,1), (3,1,1), (0,1,1)]

Hence the count = 4

# Algorithm 
1. Create a variable named count which is initialised as 0.
2. Check for the 3 conditions using a for loop
3. If it satisfies the conditions then increment the count by 1.
4. Return the count.
