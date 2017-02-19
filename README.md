# stack
bai_tap_stack.
1, countNumber:
Count natural numbers whose all permutation are greater than that number
There are some natural number whose all permutation is greater than or equal to that number eg. 123, whose all the permutation (123, 231, 321) are greater than or equal to 123.
Given a natural number n, the task is to count all such number from 1 to n.
solution:
An efficient solution is based on below observations.
Observation 1: From 1 to 9, all number have this property. So, for n <= 9, output n.
Observation 2: The number whose all permutation is greater than or equal to that number have all their digits in increasing order.
The idea is to push all the number from 1 to 9. Now, pop the top element, say topel and try to make number whose digits are in increasing order and the first digit is topel. To make such numbers, the second digit can be from topel%10 to 9. If this number is less than n, increment the count and push the number in the stack, else ignore.
