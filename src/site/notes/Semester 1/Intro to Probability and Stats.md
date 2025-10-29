---
{"dg-publish":true,"permalink":"/semester-1/intro-to-probability-and-stats/"}
---

# Link back to [[Semester 1/Home page\|Home page]]
# [Link to typed notes ](https://heogden.github.io/math1063/)


---

# 1. Into to Stats
Mean 
$$ \bar{x} = \frac{1}{n} \cdot \sum{x_n}$$
Median: the middle value in an ordered list of observations 
Model the most frequent value in the data

**SSE** = sum of squares of errors 

$$ SSE(a) = \sum_{i=1}^{n} (x_i -a)^2 $$

**SAE** = sum of absolute errors

$$ SAE(a) = \sum_{i=1}^{n}  |x_i -a| $$

### Theorem: $\bar{x}$ minimizes the SSE 
![Pasted image 20251002173706.png](/img/user/Pasted%20image%2020251002173706.png)

### Theorem: median minimizes the SAE 

The main idea is to look at slopes.. and then just find the value where the gradient changes from negative to positive

Proof is long and convoluted, link to it here, at some point it will make sense, until then, link **[here](https://heogden.github.io/math1063/index.html#measures-of-location)** 

## Measures of spread 

IQR = Interquartile range, difference between $Q_1$ and $Q_3$ 

The variance is: 
$$ Var(x) =  \frac{1}{n-1} \sum_{i-1}^{n} (x_i - \bar{x})^2 = \frac{1}{n}( \sum_{i=1}^{n} x_i^2 - n \bar{x}^2 )$$

Notice how the  $SSE(a) = \sum_{i=1}^{n} (x_i -a)^2$

And we found SSE is minimized at $a= \bar{x}$ 

So 
$$ \sum_{i-1}^{n} (x_i - \bar{x})^2 = SSE(\bar{x}) $$
To calculate the mean, we just divide by the the total population: $n-1$
There is a reason we do $n-1$, it gives us an unbiased estimate of the sample variance - this is covered later in the course 

### Proof of variance (not examined by still good for understanding)

However, there is a more useful form of the variance, the proof of which is given below: 

$$ \sum_{i-1}^{n} (x_i - \bar{x})^2 = \sum_{i=1}^{n} (x_i^2 - 2x_i\bar{x} + \bar{x}^2) $$
Then we split the sum: 
$$ = \sum_{i=1}^{n} x_i^2 + \sum_{i=1}^{n} 2x_i \bar{x} + \sum_{i=1}^{n} \bar{x}^2 $$
As the $2\bar{x}$ is a constant, we can factor that out of the sum 
$$ = \sum_{i=1}^{n} x_i^2 - 2\bar{x} \sum_{i=1}^{n} x_i + n\bar{x}^2 $$

Now using the definition of the mean: 
$$ \bar{x} = \frac{1}{n} \sum_{i=1}^{n} x_i $$

So to rearrange 

$$ \sum_{i=1}^{n} x_i = n\bar{x} $$
$$ \sum_{i-1}^{n} (x_i - \bar{x})^2 = \sum_{i=1}^{n} x_i^2 - 2\bar{x} n \bar{x}+ n \bar{x}^2 = \sum_{i=1}^{n} x_i^2 - 2 n \bar{x}^2+ n \bar{x}^2$$ 
$$ = \sum_{i=1}^{n} x_i^2 - n \bar{x}^2 $$
Therefore: 

$$ Var(x) = \frac{1}{n}( \sum_{i=1}^{n} x_i^2 - n \bar{x}^2 ) $$
The standard deviation is the square root of variance 

$$ s = sd(x) = \sqrt{Var(x)} $$ 

---
# 2. Intro to Probability 

### Definitions 

[[Tags/Definition\|Definition]] **Random experiment**: one in which we do not know exactly what the outcome of the experiment will give. 
[[Tags/Definition\|Definition]] **Sample space** - the set of all possible outcomes. Denoted by capital $S$ 
[[Tags/Definition\|Definition]] **Event** - particular result of the random experiment, a subset of the sample space. Denoted by capital letters 

Everything that is random is denoted by a capital letters. Lowercase is where we have observed 

[[Tags/Definition\|Definition]] **Union** - $A\cup B$ - either $A$ or $B$ occurs or both occur 
[[Tags/Definition\|Definition]] **Intersect** - $A \cap B$ - both $A$ and $B$ must occur 

[[Tags/Definition\|Definition]] **Mutually exclusive** - $A \cap D = \emptyset$ - A and D have no outcomes in, i.e. cannot happen at the same time 

[[Tags/Definition\|Definition]] **Complement** - $A^`$ - all of the outcomes not in A. Note the things below: 
$$ A \cup A^` = S $$
The statement above basically means that everything in A and not A is the sample space 
$$ A \cap A^` = \emptyset $$

### Axioms of probability 

$$ P\{S\} = 1 $$
$$ 0 \leq P\{A\} \leq 1 $$
$P\{A \cup B\} = P\{A\} + P\{B\}$ provided that $A$ and $B$ are mutually exclusive 

### Combinatorics 

The entire point of this section is fairly simple: being able to count outcomes without listing them all 

There are two main questions that will determine which formula we have to use.
1. Does the order matter? If it does, then we use permutations, otherwise combinations 
2. Do we replace items after choosing? If yes, with we use the with replacement cases 

#### Permutations 

The scenario here is that we have $n$ distinct items and we want to arrange them $k$ of them in a specific order. 

Think of it like filling $k$ positions on a shelf: 
- The first sport can take $n$ choices 
- The second spot can take $n-1$ choices since the first one is already used 
- The third can take $n-2$ choices and so on... 

So the total number of ordered arrangements (aka **permutations**) is: 

$$P(n,k)  = n \times (n-1) \times … \times (n-k+1)$$
Multiply numerator and denominator by $(n-k)!$ then we get the simplified definition below
$$ P(n,k) = \frac{n!}{(n-k)!}$$

#### Combinations 

Now suppose we want to choose $k$ items from $n$ distinct ones, but the order doesn't matter. 

In other ways, when we go from permutations to combinations, we don't care what order the items are chose in, only which items were chosen. So as we've already counted the same group multiple times for every possible order with permutations, we need to divide by how many times we've 'overcounted', which is $k!$ 

$$ {n \choose k} = \frac{P(n,k)}{k!}  = \frac{n!}{(n-k)! \space k!}$$
### Conditional probability and Bayes’ Theorem 

At its simplest, probability is just chance of an event, so it's: 
$$ P(A) = \frac{ \text{ number of ways A can happen}}{\text{ total possible outcomes}} $$

Conditional probability is the probability event $A$ happening given that another event $B$ has already happening. 
The formal definition is given below: 

$$ P(B|A) = \frac{P(A \cap B)}{P(A)} $$
$$ P(A|B) = \frac{P(A \cap B)}{P(B)} $$
When we arrange, we can get: 
$$ {P(A \cap B)}= P(B|A)\space {P(A)} = P(A|B) \space {P(B)}$$


#### Bayes’ Theorem 

Now, when we know something about one conditional event, but want to know about the reverse, we can use Bayes' Theorem: 

$$ P(B | A) = \frac{P(B) \space P(A |B)}{P(A)} $$
We can derive the numerator by just substituting $A \cap B$ from the rearrangement above. 

Bayes' Theorem is used widely when in medical test scenarios as it allows people to update their belief about an event after new evidence appears. To think about using an analogy: 
- We start with a prior belief $P(B)$
- Get new evidence $P(A)$
- And then we update our belief to $P(A|B)$

### Independence

Intuitively, events $A$ and $B$ are **independent** if occurrence of one event does not affect the probability that other event occurs. 

Knowing that one event happened gives you no new information about the other. 

Notice how this is different to **mutually exclusive**, which means that both events cannot happen at the same time, so $P(A \cap B) = 0$

Formally, 
If $$ P(B|A) = P(B) \text{ or } P(A|B) = P(A)$$
Then 
$$ P(B|A) = \frac{P(A \cap B)}{P(A)} = P(B)$$
$$ P(A \cap B) = P(A) P(B) $$

### Proof of Independence of complementary events

If $A$ and $B$ are independent, so are $A^`$ and $B^`$ 

We want to show the following below: 
$$P(A^` \cap B^`) = P(A^`) P(B^`) $$
$$ P(A^` \cap B^`) = 1 - P(A \cup B) $$
And how using using the general addition rule, we can rewrite the above as 
$$ = 1 - [P(A) + P(B) - P(A \cap B)] $$
Given that $A$ and $B$ are independent, we can make the substitution
$$ = 1 - P(A) - P(B) + P(A)P(B)$$
This can be factorise as: 
$$ = [1 - P(A)] [1-P(B)]$$
Which simplifies to $P(A^`) P(B^`)$

---

# 3. Probability Distributions 

Random variables are denoted by uppercase letters, like $X, Y, Z$ 

A random variable is just a mapping from the outcomes space to the reali line, so the combined probability of all values of a random variable is 1 

## Discrete Random Variable (DRV)
[[Tags/Definition\|Definition]]
**DRV**  - discrete random variable. If a random variable has a finite value 

A DRV takes specific values, like heads in coin flips and we can count how many outcomes there are. We assign probabilities to each value individually: 
$$ P(X = x_{i})$$
And so to find the total probability up to some value $k$, we just need to sum the DRVs: 
$$ P(X \leq k) = \sum_{x_{i} \leq k}P(X = x_{i})$$

For a DRV, we define a function $$ f(x) = P(X=x) $$
The function $f(x)$ is just the **probability mass** (**pmf**) or the probability function. As the total probability must be 1 and all probabilities must be non-negative, we need: 
- $f(x) \geq 0 \space \forall x$
- $\sum_{\forall x} f(x) = 1$

## Continuous Random Variable (CRV)
[[Tags/Definition\|Definition]] 
**CRV** - Continous random variable. When a variable can take any value on the real line

There are infinitely many possible values, so the probability of hitting any exact number, $P(X=x) = 0$

So instead, we can talk about densities, the probability per unit of $x$ 

## Probability Density Function (PDF)

This function essentially tells us how densely probability is packed around each value. 
This is defined as: 
$$ P(a \leq X \leq b) = \int_a^bf(x) dx $$
That's why for CRVs, integration replaces summation, it's the continuous version of adding up infinitely small pieces. 

For the pdf, we need: 
- $f(x) \geq 0 \space \forall x$
- $\int_{- \infty}^{\infty} f(x) dx = 1$ 

## Cumulative distribution function (CDF)

This function calculates the probability of the random variables up to its arguments: 

$$ F(x) = P(X \leq x) $$
For a DRV, it's defined as: 

$$ P(X \leq x) \equiv F(x) = \sum_{x_{i} \leq x} P(X = x_{i}) $$

And for a CRV, the CDF is defined as: 

$$ P(X \leq x) \equiv F(x) = \int_{-\infty}^x f(t)
 dt $$
So the CDF is essentially the area under the PDF curve up to $x$ 

### Relationship between PDF and CDF 

For a CRV, the PDF is the derivative of the CDF 

If $$F(x) = \int_{-\infty}^x f(t) dt $$
And we differentiate both sides with respect to $x$ we get: 

$$ f(x) = \frac{d \space F(x)}{dx} $$

What this tells us that the PDF is just the slope of the CDF. Where the CDF rises, the PDF is large, lots of probability density there. And where the CDF is flat, the PDF is small. 
## Expectation 

Think of expectation (or the expected value) as the long-run average value of a random variable if you repeated the experiment infinitely many times. 

For example, if you roll a fair rice, the values are in the set of $[1,6]$ 
Each roll has probability $1/6$. 
Then 
$$ E[X] = 1 \cdot \frac{1}{6} + 2 \cdot \frac{1}{6} + \dots + 6 \cdot \frac{1}{6} = 3.5 $$
You'll never roll a $3.5$, but if you roll hundreds of times, you average approaches $3.5$

### Formal definition 

For a DRV with possible values $x_1, x_2 ... x_n$,  and probabilities $p_i = P(X = x_i)$: 

$$ E[X] = \sum_{i} x_{i}p_{i} $$
And for CRV with PDF $f(x)$: 

$$ E[X] = \int_{- \infty}^{\infty} x f(x) dx$$

Same idea, we're just replacing the sum with an integral because now the variable takes infinitely many values 

### Expectation of a uniform distribution function 

Say we have $X \sim U(a,b)$, a uniform distribution where each probability is equally likely anywhere between $a$ and $b$ 

The PDF is: 
$$
f(x) = 
\begin{cases}
\frac{1}{b-a}, a \leq x \leq b \\
0, \text{ otherwise } 
\end{cases}
$$
Then the expectation is: 

$$ E[X] = \int_{a}^{b} x \frac{1}{b-a} = \frac{1}{b-a}\left[ \frac{x^2}{2} \right]_{a}^{b} = \frac{a+b}{2}$$
Which is just the midpoint of the interval 

### Expectation of a function 

If you have some function of the random variable say $Y = g(X)$, then it's expectation is 

- Discrete: 
$$ E[g(X)] = \sum_{i} g(x_{i}) p_{i} $$
- Continuous: 

$$ E[g(X)] = \int_{-\infty}^{\infty} g(x) f(x) dx$$
This is extremely useful as it lets us find things like: 
- $E[X^2]$  which is later needed for variance 
- $E[\sin x]$
- etc. 

### Linearity of expectation 

this is probably one of the most useful properties in probability. 
For any random variable $X$, $Y$, and constants $a,b$: 

$$ Y = aX + b$$

$$  E(Y) = aE(X) +b$$

The reason we can do this is because expectation acts like a weighted average. If we stretch all our data by a factor of $a$, then the average stretches by $a$, and then if we shift all the data by $b$, the average shifts by $b$. 

#### Proof of linearity 

For a DRV: 
$$ E[Y] = \sum_{y} y P(Y=y)$$
But since $Y = aX + b$, we can rewrite the above expression as: 
$$ E[Y] = \sum_{x} (ax+b) P(X=x) $$
And now we can distribute the sum: 
$$ E[Y]= a \sum_{x}x P(X=x) + b \sum_{x}P(X=x)$$
The first part of the sum is just $a E[X]$ by definition of expectation, and the second part is $b(1)$ since the probabilities sum to $1$. 
So we have: 
$$ E[Y] = aE[X] + b$$

For a CRV: 
$$ E[Y] = \int_{-\infty}^{\infty} y f(y) dy $$
And again, as $Y = aX + b$, we can write it as: 

$$ E[Y] = \int_{- \infty}^{\infty} (ax+b) f(x) dx$$

$$ = a\int_{-\infty}^{\infty} xf(x) dx + b \int_{- \infty}^{\infty} f(x) dx $$
The first part is again just $aE[X]$ by definition and the second part equals $1$ since the total probability is $1$. 

Note on notation here: capital $X$ represents the random variable, i.e the function that maps outcomes to numbers. And an $x$ represents a value that $X$ might take. So when we're computing the expectation of $E[Y]$, we're summing or integrating over all the possible values it can take, so we replace $X$ with $x$. 

### Expectation of symmetric random variable 

A random variable $X$ is called symmetric about a point $c$ if its PDF (or PMF) satisfied: 
$$ f(c+x) = f(c-x) \space \forall x > 0 $$
If $X$ is symmetric about $c$, then $E(X) = c$

Intuitively, think of this as the centre of mass of the function. If the PDF or PMF is symmetric about a point $c$, then for every value to the left of $c$, there's an equal value to the right of $c$ with the same probability. This property saves us from having to do nasty integrals when finding expectations. 

#### Proof for symmetric random variable 

First, let $Y = X - c$. This means that $Y$ is symmetric about $0$, so our PDF satisfies the following property of an even function: 

$$ f(y) = f(-y) \space \forall y > 0$$

Then we have: 

$$ E(Y) = \int_{-\infty}^{\infty} y f(y) dy$$
$$ = \int_{-\infty}^{0} y f(y) dy + \int_{0}^{\infty} y f(y) dy $$
We can substitute $z = -y$ and flip the integral limits to get: 
$$ = \int_{0}^{\infty} -z f(-z) dy + \int_{0}^{\infty} y f(y) dy $$
As as $f(-z) = f(z)$ 
$$ = - \int_{0}^{\infty} z f(z) dy + \int_{0}^{\infty} y f(y) dy $$
$$ = 0 $$

## Variance 

We already saw that the expectation $E(X)$ is the long run average of $X$. Now, if we want to do know how spread out the values are from the mean, we can use the variance. 

If we wanted to measure how far (deviated) each possible value of $X$ is from the mean, that's $X - E(X)$. But if we took lots of samples from the population, we could average those deviations. But the positive and negatives ones cancel, so we instead square them to get the magnitude: 

$$ Var(X) = E(X - E(X))^2$$
For very large $n$, we know that $\bar{x} \approx E(X)$, as for a large enough sample, the sample mean gets closer to the actual mean. So if we write $\mu= E(X)$, the sample variance is: 

$$ \approx \frac{1}{n} \sum_{i=1}^{n} (x_i - \mu)^2 $$
So when $n$ is large, this will be close to : 
$$ E(X-\mu)^2 $$

This variance is therefore defined by: 

$$ Var(x) = E(X-\mu)^2 = \begin{cases}

\sum_{\forall x} (x-\mu)^2 f(x) \text{ if X is discrete } \\

\int_{-\infty}^{\infty}(x-\mu)^2 f(x) dx \text{ if X is continuous}

\end{cases}

$$


### Proving variance 

There is a more useful form of variance, which we can prove from the definition below: 
$$ Var(X) = E[(X-E(X))^2] $$
After expanding the bracket
$$   (X - E(X))^2 = X^2 - 2XE(X) + (E(X))^2$$
Take the expectation of both sides: 
$$ E[(X-E(X))^2]  = E[X^2 - 2XE(X) + (E(X))^2]$$
Using the linearity of expectation, we can split and pull constants out to geT: 
$$ = E(X^2) - 2E(X)E(X)  + (E(X))^2$$
After simplifying we have: 
$$ Var(X) = E(X^2) - (E(X))^2  $$
$$ \equiv E(X^2) - \mu^2 \text{ where } \mu^2 = (E(X))^2$$

### Linearity of variance 

If $Y = aX + b$, then 
$$ E(Y) = aE(X) + b$$
$$ Var(Y) = a^2 Var(X)$$
- Scaling by $a$ stretches or shrinks the spread 
- Adding $b$ shifts everything, so no change in spread 

To prove this, we can use the definition of variance and some algebra 
$$ Var(Y) = E[Y - (E(Y))^2] $$
After substituting in for $E(Y)$ using the linearity of expectation we have: 
$$ = E[(Y - (aE(X)+b))^2]$$
$$ = E[((aX+b) - aE(X) -b)^2] $$
We can do some cancelling of the $b$ to get: 
$$ = E[a^2 (X-E(X))^2] $$
As $(X - E(X))^2 = Var(X)$ by definition, we have: 
$$ Var(Y) = a^2 Var(X)$$
$$\square$$

## Sample median of random variables 
### Quantiles 

For any $0 < p< 1$, the $p$-quantile $q$ solves $F(q) = p$. So if $F$ is invertible, then $q = F^{-1} (p)$

## Standard Discrete Distributions 

### Bernoulli Distributions 

**Bernoulli trails** are a name for a set of independent trials, where each trial has only two possible outcomes- success, and failure. 

For a Bernoulli trial: 

$$  X = \begin{cases}
1 \text{ if S} \\
2 \text{ if F}
\end{cases}
$$
$X \sim$ Bernoulli($p$) 

The Bernoulli distributions has pmf: 
$$ f(x) = P(X=x) = p^x(1-p)^{1-x},  \space x = 0,1$$
For this distribution, the expectation is: 

$$E(X) = \sum_{x} xf(x) = p $$
$$ E(X^2) = \sum_{x} x^2f(x) = p $$
And the variance is: 
$$ Var(x) = E(X^2) - \mu^2 = p - p^2 = p(1-p),\space  \mu = E(X)$$
### Binomial distribution 

Defined as:  

$$ X \sim B(n,p) $$
If $X$ is the number of successes ($S$) out of $n$ Bernoulli trials 

#### PMF for the Binomial 

To find the PMF, we want to find $f(x) = P(X=x)$, i.e. the probability of $x$ Successes, and $(n-x)$ Failures 

The probability of the outcomes can be given by: 
$$ P(SS…FS…SF)  = pp \cdots (1-p)p \cdots p(1-p) =  {n \choose k} p^x(1-p)^{n-x}$$
So to generalize, 
The pmf is: 

$$ f(x) = P(X=x) ={n \choose k} p^x(1-p)^{n-x} , \space x = 0,1,…n$$
Now one might wonder how we know that $$ \sum_{x=0}^{n}f(x) = 1$$
… by using the binomial theorem 

$$ (a+b)^n = b^n{n \choose 1} ab^{n-1} +{n \choose 2}a^2b^{n-2} + \cdots +a^n $$
$$ = \sum_{x=0}^{n} {n \choose x} b^{n-x} a^{x}$$
Now if we choose $a =p$ and $b = (1-p)$, then 

$$ \sum_{x=0}^{n} {n \choose x} p^x(1-p)^{n-x} = 1 $$

### Expectation and Variance of a Binomial function 

Intuitively, think of $X$ (the total number of successes) as being made up on $n$ smaller random variables, one for each trial 

Let 
$$ X = X_{1} + X_{2} + X_{3} + \dots + X_{n}$$
Where $X_i$ is $1$ if the trial is a success and $0$ if the trial is a failure. So each $X_i$ is a Bernoulli random variable with parameter $p$ 

Now, we know that for a single trial, the expectation of a Bernoulli variable is 
$$ E(X_{i}) = 1(p) + 0(1-p) = p$$
And since each expectation is linear, the expectation of the sum is 
$$ E(X) = E(X_{1} + X_{2} + \dots + X_{n}) = E(X_{1}) + E(X_{2}) +\dots +E(X_{n})$$
Where each $E(X_i) = p$ 

So we get that expectation of a binomial is 
$$ E(X) = np$$
The variance is 
$$ Var(X) = np(1-p)$$

The proof of this is left as an exercise to the reader 
## Geometric Distribution 

Intuitively, the geometric distribution is the first one that captures the "keep trying until you succeed" idea. So imagine we're running an experiment where: 
- Each trial is independent 
- Each trial has a probability of success $p$ 
- We keep repeating until we get our first success

The random variable $X$ represents the trial number on which the first success occurs. 

### PMF for a geometric distribution 

To get a success on the $x$-th trial, we must have $(x-1)$ failures first, followed by $1$ success. Each success has a probability of $p$ and each failure has a probability of $(1-p)$ 

$$ P(X=x) = (1-p)^{x-1}p, \space x = 1,2,3$$

### CDF 

$$P (X \leq x) =  1-(1-p^x), \quad P(X> x) = (1-p)^x$$

Note - R assumes the number of failures until first success, instead of the number of trials until the first success. So if $X \sim Geo(p), X-1$ is the number of failures 
### Memoryless distribution 

The geometric distribution is memoryless, i.e 
$$ P(X > s +k \space | X > k) = P(X > s) $$

This means just that the probability we still have to wait for $s$ for more trials doesn't depend on how long we've already waited for. No other discrete distribution has this property! 
### Expectation of a geometric distribution 

For the intuition, imagine playing a game where: 
- Every trial has a chance $p$ of success 

How many tries do we expect to need before success? 

If $p$ was large, then we'd succeed quickly, resulting in a small expected $X$ 
If $p$ was small, then we would have to wait much longer, so a large expected $X$ 

So the average should: 
- Decrease when $p$ increases 
- Increase when $p$ decreases 
$$ E(X) = \frac{1}{p} $$
The proof involves using negative binomial series, something which will not be covered in lectures, but it’s in the notes. A much nicer proof is covered in 2nd year Statistical Inference module 

### Variance of a geometric distribution 

Going back our previous analogy, the variance here is how spread out the time between our successes. So if $p$ was big, we would succeed quickly, resulting in a smaller variance. And if $p$ was small, we could have to wait a long time, so a big variance 

$$ Var(X) = \frac{1-p}{p^2}$$

## Hypergeometric Distribution 

This distribution is all about sampling without replacement, i.e. the realistic binomial 

Suppose we have a population of $N$ total individuals: 
- A proportion $p$ are of type $S$ (success)
- The remaining $1-p$ are of type $F$ (failures)

So the total number of type $S$ individuals is $Np$ and type $F$ is $N(1-p)$

Now, we want to sample $n$ individuals without replacement. Let $X$ = the number of type $S$ Is our sample, then $X$ follows a hypergeometric distribution: 

$$ X \sim HypGeo(N, n, p)$$
Then it's PMF is given by: 
$$ f(x) = P(X=x) = \frac{{Np \choose x}{N(1-p) \choose n-x}}{N \choose n} \quad x = 0,1,2\dots n$$

The numerator counts how many ways to get exactly $x$ succeses, and $n-x$ failures, and the denominator normalises so that the probabilities sum to 1 


### Expectation 

$$ E(X) = np$$
Notice how the expectation is the same as the binomial distribution, and that's because we are drawing without replacement 
### Variance 

$$Var(X) = np(1-p) \frac{N-n}{N-1} $$

## Negative Binomial Distribution 

The negative binomial distribution models the number of trials needed to achieve a fixed number of successes, $r$ in independent Bernoulli trials. In other words, it's how long till we get $r$ successes. 

If we just wanted $1$ success, then the negative binomial is the same as the geometric distribution, which stop when we get our first success. 

$$ NegBin(r=1, p) \equiv Geo(p) $$
### PMF 

Imagine flipping a coin where $p=0.3$ of getting heads. And we want to know how many flips it will takes to get 3 heads. That random variable $X$ follows a negative binomial distribution, the PMF for which is given by: 

$$ X \sim NegBin(r,p)$$
$$ f(x) = P(X=x) = {{x-1} \choose {r-1}} (1-p)^{x-r}p^r, \quad x = r, r+1…$$

### Expectation 

Each success takes $1/p$ trials on average, and we need $r$ of them

$$ E(X) = \frac{r}{p}$$

### Variance 

$$ Var(X) = r\frac{1-p}{p^2}$$


