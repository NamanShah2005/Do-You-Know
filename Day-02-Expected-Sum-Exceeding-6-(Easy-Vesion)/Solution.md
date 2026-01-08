# Solution

Let S be the Sum before the last throw.

Let D be the value on the last throw.

Therefore X = S + D ....(1)

Clearly, S ≤ 6 .....(2) (Since S is the sum before the final throw, and we stop only after sum exceeds 6)

Also, S + D > 6 ....(3) (Since D is the value on the final throw, that means, after it, we are stopping, so S + D > 6)

Hence, from (2),

S ∈ {1, 2, 3, 4, 5, 6}

*NOTE : S can't be 0, since D is the final throw, therefore D ∈ {1, 2, 3, 4, 5, 6}, and S+D > 6, Hence, S can't be 0, which means there should be atleast one throw, before the final throw.*

**Let's condition on S**

i.e. E[X|S = s]

Let S = 5

Therefore, D can be {2, 3, 4, 5, 6} (Since, S + D > 6)

Since All are equally Likely,

Average of these : (2 + 3 + 4 + 5 + 6)/5 ​= 4

Hence, E[X|S = 5] = E[(S + D)|S = 5] = E[S|S = 5] + E[D|S = 5]

5 + $\sum_{x=2}^{6} x\,p(x)$

5 + $\frac{1}{5}\cdot2 + \frac{1}{5}\cdot3 + \cdots + \frac{1}{5}\cdot6$

(NOTE : We Divided by 5 and not by 6, this is because, we have condition that S = 5, and only final role is ;eft, hence, value will only be one of {2, 3, 4, 5, 6}, and never 1)

5 + 4 = 9

Similarly,

E[X|S = 1] = 7

E[X|S = 2] = 7.5

E[X|S = 3] = 8

E[X|S = 4] = 8.5

E[X|S = 5] = 9

E[X|S = 6] = 9.5

Hence, final Answer = (7 + 7.5 + 8 + 8.5 + 9 + 9.5)/6 = 8.25

## **Where did the Assumption given in the Question helped?**

### **(Assumption was : Assume that the cumulative sum immediately before exceeding 6 is uniformly distributed over {1, 2, 3, 4, 5, 6}).**

We Calculated

E[X|S = 1] = 7

E[X|S = 2] = 7.5

E[X|S = 3] = 8

E[X|S = 4] = 8.5

E[X|S = 5] = 9

E[X|S = 6] = 9.5

But the problem came in the next step, where we wrote

Hence, final Answer = (7 + 7.5 + 8 + 8.5 + 9 + 9.5)/6 = 8.25

Since,

S = 1 can be in a single way, throwing Die a single time and getting 1 i.e (1)

S = 2 can be in more ways, throwing die a single time and getting 2, or throwing a die 2 times and getting 1 on each i.e (2), (1,1)

S = 3 can have (3), (2,1), (1,2), (1,1,1), Similarly for others.

This means S=1 is less likely than S=6, and here our assumption helps by **Assuming that the cumulative sum immediately before exceeding 6 is uniformly distributed over {1, 2, 3, 4, 5, 6}**