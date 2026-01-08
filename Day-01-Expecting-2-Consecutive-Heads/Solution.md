# **Solution**

Let:

- E₀ = expected tosses to get two consecutive heads, starting with no prior heads
- E₁ = expected tosses to get two consecutive heads, given one head already observed

We want to find E₀

From state E₀:
- With probability 1/2, we get a tail and remain in E₀
- With probability 1/2, we get a head and move to E₁

Hence:
E₀ = 1 + (1/2)E₀ + (1/2)E₁  .....(1)

From state E₁:
- With probability 1/2, we get a head and finish
- With probability 1/2, we get a tail and return to E₀

Hence:
E₁ = 1 + (1/2)·0 + (1/2)E₀

Therefore, 
E₁ = 1 + (1/2)E₀  ........(2)

Solving the system (1) and (2) gives:
E₀ = 6

Therefore, the expected number of tosses is **6**.