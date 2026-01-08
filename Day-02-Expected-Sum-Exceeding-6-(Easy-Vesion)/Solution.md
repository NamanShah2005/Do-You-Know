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




# Solution

We roll a fair die repeatedly until the **cumulative sum first exceeds 6**.

Let:
- **S** = cumulative sum *before* the final throw  
- **D** = value obtained on the final throw  
- **X** = final sum

Then,
\[
X = S + D \tag{1}
\]

---

## Properties of \( S \) and \( D \)

Since \( S \) is the sum *before* the final throw:

\[
S \le 6 \tag{2}
\]

We stop immediately after the sum exceeds 6, so:

\[
S + D > 6 \tag{3}
\]

From (2) and (3), it follows that:
\[
S \in \{1,2,3,4,5,6\}
\]

> **Note:**  
> \( S = 0 \) is not possible.  
> Since \( D \in \{1,2,3,4,5,6\} \) and \( S + D > 6 \), there must be **at least one roll before the final roll**.

---

## Conditioning on \( S \)

We compute:
\[
\mathbb{E}[X \mid S = s]
\]

---

### Case: \( S = 5 \)

For \( S = 5 \), the final throw must satisfy:
\[
D \in \{2,3,4,5,6\}
\]

All these outcomes are equally likely.

The average value of \( D \) is:
\[
\frac{2 + 3 + 4 + 5 + 6}{5} = 4
\]

Hence,
\[
\mathbb{E}[X \mid S = 5]
= \mathbb{E}[S + D \mid S = 5]
= 5 + \sum_{x=2}^{6} x\,p(x)
\]

\[
= 5 + \left(\frac{1}{5}\cdot2 + \frac{1}{5}\cdot3 + \cdots + \frac{1}{5}\cdot6\right)
\]

\[
= 5 + 4 = 9
\]

> **Note:**  
> We divide by **5**, not **6**, because under the condition \( S = 5 \),  
> the value \( D = 1 \) is impossible.

---

## Computing \( \mathbb{E}[X \mid S = s] \) for all \( s \)

Using the same reasoning:

\[
\mathbb{E}[X \mid S = 1] = 7
\]

\[
\mathbb{E}[X \mid S = 2] = 7.5
\]

\[
\mathbb{E}[X \mid S = 3] = 8
\]

\[
\mathbb{E}[X \mid S = 4] = 8.5
\]

\[
\mathbb{E}[X \mid S = 5] = 9
\]

\[
\mathbb{E}[X \mid S = 6] = 9.5
\]

---

## Final Expectation

Assuming that the value of \( S \) is **uniformly distributed** over  
\(\{1,2,3,4,5,6\}\), we compute:

\[
\mathbb{E}[X]
= \frac{7 + 7.5 + 8 + 8.5 + 9 + 9.5}{6}
= 8.25
\]

---

## Where Did the Given Assumption Help?

### **Assumption:**
> *The cumulative sum immediately before exceeding 6 is uniformly distributed over*  
> \(\{1,2,3,4,5,6\}\).

We calculated:
- \( \mathbb{E}[X \mid S = 1] \)
- \( \mathbb{E}[X \mid S = 2] \)
- \( \dots \)
- \( \mathbb{E}[X \mid S = 6] \)

However, a difficulty arises when averaging these values.

For example:
- \( S = 1 \) can occur only as:  
  \((1)\) i.e. throwing Die a single time and getting 1
- \( S = 2 \) can occur as:  
  \((2), (1,1)\) i.e. throwing die a single time and getting 2, or throwing a die 2 times and getting 1 on each
- \( S = 3 \) can occur as:  
  \((3), (2,1), (1,2), (1,1,1)\)

Thus, **larger values of \( S \) are naturally more likely** than smaller ones.

The assumption resolves this issue by **forcing all values of \( S \) to be equally likely**, which justifies taking a simple average of the conditional expectations.

---

## ✅ Final Answer

\[
\boxed{\mathbb{E}[X] = 8.25}
\]
