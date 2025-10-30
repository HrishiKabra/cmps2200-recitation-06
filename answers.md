# CMPS 2200 Recitation 06
## Answers

**Name:** Hrishi Kabra  
**Name:** Petra Radmanovic


Place all written answers from `recitation-07.md` here for easier grading.



- **2)**

For the recursive implementiaton of the fibonacci sequence, each time we call the imput prior and two prior, and do constant work at each level. So $W(n) = W(n-1) + W(n-2) + O(n)$

each time, the number of calls doubles. this means when we start with 1 number, we then go to 2, then to 4, for as many levels as n is. So, the work $\in O(2^n)$

- **3)**

The span would be the max of the two calls, meaning whether the n-1 or n-2 call takes more work. Meaning $S(n) = \text{max}(W(n-1) + W(n-2))$. Since n-1 will usually take more work, we simply do 1 + 2 + 3... n or $S(n) \in O(n)$

- **4)**

Each time the recursive fibbonacci is run, counts keeps track of how many times a certain fibonacci number is called. For example, when n = 10 is run, counts is [34, 55, 34, 21, 13, 8, 5, 3, 2, 1, 1] - counts list forms the fibonacci sequence in reverse This shows that the values of fibbonacci follow a reverse fibbonacci themselves, where the two numbers callsed first happen once, and the third number is called the sum # of times except for the final value, or for 0. This is likely because the first base case can get hit by both the n-1 call and the n-2 call, while the 0 base case can only be hit by the n-2 case.

- **6)**

Each value F_i is computed at most once - it can be called by i+1 and i+2 hence maximum number of times fib_top_down is called for any i is 2 - one call that computes it and at most one later call that retrieves it - hence total work is O(n) and span is O(n)

- **8)**

In bottom-up method each F_i is read O(1) times - at most twice to compute F_i+1 and F_i+2 - hence work = O(n) and span = O(n)