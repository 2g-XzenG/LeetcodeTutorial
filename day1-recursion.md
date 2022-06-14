## Recursion

Appearance: function calls itself

Essence: split a big problem into smaller ones

Implementation:
- base case: smallest problem to solve
- recursive rule: how to make the problem smaller
    - how to split into smaller problems
    - how to combine the smaller problems
        
     
[LC509. Fibonacci Number](https://leetcode.com/problems/fibonacci-number/)

```
def fib(n):
    if n == 0: 
        return 0
    if n == 1: 
        return 1
    return fib(n-1) + fib(n-2)


Time: O(2^n)
Space: O(n)
```

Analysis: [recursive tree graph](https://www.google.com/search?q=recursion+tree+fibonacci&rlz=1C5GCEM_enUS1007US1007&sxsrf=ALiCzsbgwZIM4rTxthiD_9cLGtrDfdkSAg:1655169274445&source=lnms&tbm=isch&sa=X&ved=2ahUKEwihzpWF4qv4AhUWoXIEHceCBp8Q_AUoAXoECAEQAw&biw=1636&bih=1336#imgrc=qi3tB9aX6WZ52M)


[50. Pow(x, n)](https://leetcode.com/problems/powx-n/)

```
class Solution:
    def myPow(self, x, n):
        if abs(x) < 0: 
            return 0 
        if n == 0: 
            return 1
        if n < 0: 
            return self.myPow(1/x, -n)
            
        half = self.myPow(x, n//2)
        if n % 2 == 0: 
            return half*half
        if n % 2 == 1: 
            return half*half*x
            
Time: O(logn)
Space: O(logn)            
```
        
