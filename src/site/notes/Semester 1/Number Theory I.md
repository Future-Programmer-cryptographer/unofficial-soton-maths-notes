---
{"dg-publish":true,"permalink":"/semester-1/number-theory-i/"}
---


# [Link to typed lecture notes](https://blackboard.soton.ac.uk/ultra/courses/_233973_1/outline)

# Intro...  [HTML version ](https://www.southampton.ac.uk/~wright/1001/)


- Dr Nick Wright - Regular office hrs from week 3 on Mondays - 1-2pm 
	- Contact email: wright@soton.ac.uk or teams 
	- Put MATH1001 in the subject line! 
- Coursework- 20% 
	- Set on Thurs, due the following Tues 
	- Only 1 exercise marked, 2nd set for practice purposes 
	- Self-marking + submit again 
- class test: 10% 
	- Friday, 21st Nov 
	- Paper test -  closed book 
	- Last year’s class test will be on blackboard 
- Final exam: 70% 
	- Sometime in January  

- Study integers and aim to prove results about integers  
- How to prove numbers are transcendental like $\pi$ or $e$ [[Tags/questions\|questions]]

Consider the problem below: 

$$p \text{ is prime iff } (p-1)! \text{ is divisible by } p$$
or this one - we might cover this if we have time… 
$$ \text{There are infinitely many integer solutions to the equation } a^2 + b^2 = c^2 \text{ where a, b, c have no common factors} $$

- How can people even get started with proving this stuff.. like with Fermat- where on earth do you start? [[Tags/questions\|questions]] 

---
# Introduction to Proofs and Logic 

[[Tags/Definition\|Definition]] A **statement** (or proposition) is an expression that can be assigned the value of true or false 

Anything that’s a question is not a statement. 
In the example below, it’s a statement cuz the variable is “used up”. We really need to specify what’s happening to the variable for it to be a statement.  $$ \sum_{i=1}^{4} i=10 $$

[[Tags/Definition\|Definition]] A **predicate** is a ‘statement’ whose truth is dependent on one or more variables 
- For a predicate, the variable is not “used up” 

$$ \sum_{i=1}^{n} i=10 $$

[[Tags/Definition\|Definition]] A **variable** is a placeholder which gives a name to some entity that we want to consider 

We can turn a predicate into a statement by specifying the set of values it applies to. Consider the example below: 
This is a predicate unless we specify $\forall n, \in \mathbb{Z}$
$$ \sum_{i=1}^{n} i= \frac{n(n+1)}{2} $$
[[Tags/Definition\|Definition]] A **set** is a collection of elements which can be any type of mathematical objects 

- A set of sets that contains no set? - Russel’s paradox 
- How is a collection not a set? [[Tags/questions\|questions]] 
	- Let S be the collection of all sets that are not members of themselves (not a set)??

## Set notation 

The notation $x \in X$ means that $x$ is an element of the set $X$. 
Eg: $n \in Z$ means $n$ is an element of the set of integers 

Building a subset: 
If $P(x)$ means $x$ is even, then this subset below is just the set of even number 
$$ \set{x \in X : P(x)} $$


[[Tags/Axiom\|Axiom]] If all $x \in A$ are also in $B$ and all $x\in B$ are also in $A$ then $A$ and $B$ are the same set.  

 - Proper subset ($\subset$) - Every element of $A$ is also in $B$ but not equal to $B$
 - Subset ($\subseteq$) - Set $A$ is a subset of $B$ if every element of $A$ is also in $B$

## Quantifiers - they help us turn predicates into statements 

$P(n)$ Is a predicate  
But $\forall n \in \mathbb{Z} \space \exists P(n)$ is a statement 

**Universal quantifier**

$$ \forall n \in \mathbb{Z} \space n^2 \geq 0 $$
The expression above in words means “for every integer $n$, $n^2$ is greater than or equal to 0”

**Existential quantifier**

$$ \exists n \in \mathbb{Z} \space  n^2 = 289 $$
“There exists at least integer $n$ such that $n^2$ is 289 

## Logical operators 
Probably the best way to think about these, is to form a truth table (warning: may trigger past CS trauma…) - think of True as 1 and False as 0, binary 

[[Tags/Definition\|Definition]]

1. **Conjunction** - both statements are true - like the AND logic gate 

$$ P \wedge Q $$
| P   | Q   | P $\wedge$ Q |
| --- | --- | ------------ |
| 0   | 0   | 0            |
| 0   | 1   | 0            |
| 1   | 0   | 0            |
| 1   | 1   | T            |

2. **Disjunction** - at least one statement is true - like the OR logic gate 

$$ P \vee Q $$

| P   | Q   | P $\vee$ Q |
| --- | --- | ---------- |
| 0   | 0   | 0          |
| 0   | 1   | 1          |
| 1   | 0   | 1          |
| 1   | 1   | 1          |
3. **Negation** - the statement is false - like the NOT logic gate 

| P   | $\neg$ P |
| --- | -------- |
| 0   | 1        |
| 1   | 0        |

---
[[Tags/Definition\|Definition]]. **Tautology**: A statement that is always true 
[[Tags/Definition\|Definition]]  **Contradiction**: A statement that is always false 

Logical equivalent - two statements have the same truth table

$$ P \equiv Q $$
## Rules - flashback to AQA CS being actually useful 

- **Idempotent** - something that squares to itself 
	- Eg: $0^2 = 0$ or $1^2 =1$
- Notice how there’s a difference between associative and distributive 
	- Associate - the symbol is the same all the way 
	- Distributive - it’s like mixing the signs for $\times$ and $+$

### Proving the De Morgan’s Laws - on Anki 

“Break the line, change the sign” 

- Well, you can do it using truth table, or Venn diagram probably 

Think about this analogy, let $P$ be the statement: “A in even” and $Q$ be the statement: “Q is even”. 

Then $P \wedge Q$ would be the statement: A is even and B is even 
If we were to negate that statement, i.e $\neg (P \wedge Q)$ would be result in the statement: “Either one of A or B is not even” 

So $$ \neg (P \wedge Q) = (\neg P) \vee (\neg Q)$$
Consider the **absorption rule** below

$$ P \wedge (P \vee Q) \equiv P $$
$$ P \vee (P \wedge Q) \equiv P $$
But how can we prove this? 
Think back to the **identity** rule where we had: $$ P \equiv P \wedge T $$
So we have 
$$ P \vee (P \wedge Q) \equiv (P \wedge T) \vee (P \wedge Q)  $$
After substituting, we can use the **distributive** rule, to factorise this: 
$$ (P \wedge T) \vee (P \wedge Q) \equiv P \wedge (T \vee Q) $$
Note, $T \vee Q \equiv T$ (**annihilation rule**), so we’re left with $P$ given the identity rule 
Another way to think about it: $T \vee Q \equiv (Q \vee \neg Q) \vee Q$
Then after using **communicative** and **associate** rules by moving the brackets around, we have: $$ (Q \vee Q) \vee (\neg Q) $$
Then by the **idempotent** rule: $Q\vee Q \equiv Q$
And then $Q \vee \neg Q \equiv T$
Look at the gold example on notes… 
## Negating quantifiers 
Consider this statement below: 
$$ \forall n \in \mathbb{Z} \space n^2 \geq 0 $$
What does it mean for the statement to be false? 
It means $\exists n \in \mathbb{Z} \space s.t. n^2 < 0$

In general… 
$$ \neg (\forall n \space P(x)) \equiv \exists n \space \neg(P(x))$$

## Implications

$$ P \implies Q \equiv (\neg P) \vee Q$$
If $P$ is false, then the statement doesn’t tell us anything about $Q$, the latter can be true or false

If we know that $P \implies Q$ is true, then: 
- $P$ and $Q$ can be both true 
- $P$ is false and $Q$ is true 
- $P$ and $Q$ can be both false 

But.. if $P \implies Q$ is true and $P$ is also true, then: 
- $Q$ is also true 

This principle above is called ***modus ponens***

[[Tags/Definition\|Definition]] - A counterexample is where the first statement is true, but the second statement is false, which makes the implication false 

If we were to negate the implication, we’d get: 
$$ \neg (P \implies Q) \equiv \neg (\neg P \vee Q) $$
Using De Morgan’s, we get
$$ \equiv \neg (\neg P) \wedge \neg Q  \equiv P \wedge\neg Q$$
So a counterexample by definition is when $P$ is true and $Q$ is not true 
$$\therefore  \neg (P \implies Q) \equiv P \wedge \neg Q $$

To claim that a statement is false is the same as claiming that its **negation** is true

Consider this example in words: 
What’s the negation of $\forall p \in \mathbb{Z}, \space p$ is prime $\implies$ $2^p -1$ is prime 

$$ \exists p \in \mathbb{Z} \neg (…) $$
So this would be $\exists p \in \mathbb{Z} \space s.t. p$ is prime and $2^p -1$ is not prime 
##  Converse and Contrapositive 

[[Tags/Definition\|Definition]] **Converse** of an implication $P \implies Q$ is the reversed implication $Q \implies P$ 

[[Tags/Definition\|Definition]] **Equivalence** $P \iff Q$ is the same as $P\implies Q \wedge Q \implies P$. It’s  an if and only if statement 

[[Tags/Definition\|Definition]] **Contrapositive** of an implication $P \implies Q$ is the implication $\neg Q \implies \neg P$

$$ P \implies Q \equiv \neg Q \implies \neg P $$
Proof by contrapositive can be useful in some case. Consider the proof, $n^2$ is even $\implies n$ is even. The contrapositive version of this would be $n$ is not even $\implies$ $n^2$ is not even. So if we start by taking $n$ to be odd and then proving that $n^2$ is odd, we have our proof for the original statement. 

When $P$ is true, then $Q$ must also be true, but this also means that $Q$ is false could only happen when $P$ is false 
We can prove this using the commutative and double negation rule 

$$ P \implies Q \equiv (\neg P) \vee Q $$
Using the commutative rule we get: 
$$ \equiv Q \vee (\neg P)$$
Then using the double negation rule we have: 
$$ \neg (\neg Q) \vee \neg P$$
Notice how this is the definition of implies: 
$$ \neg Q \implies \neg P \equiv \neg (\neg Q) \vee \neg P   $$
**Modus ponens**

$$ P \wedge (P \implies Q) \equiv P \wedge Q $$

## Proofs 

[[Tags/Definition\|Definition]] A **Proof** is a sequence of steps used to demonstrate that a statement is true 

Proofs begin with a **premise**, aka a collection of statements/predicates that we accept as true (**axioms**). 

The result that we want to show is the **conclusion**

## Rules of Equality 

When we say $a = b$, it means that $a$ and $b$ refer to the same indistinguishable objects 

- **reflexive** $a = a$ 
- **symmetric** $a = b \iff b = a$ 
- **Transitive** $a = b  \wedge b = c \implies a = c$
## Proof by contradiction 

The idea behind this is to take our premise and negation of conclusion as the assumption 
The formal justification is that if we show $\neg P$ implies another false statement, then we have proved that: 

$$ \neg P \implies F $$
And by using our logical equivalences 

$$ \neg P \implies F  \equiv \neg(\neg P) \vee F \equiv P \vee F \equiv P$$
So if we have problem that the negation is false, then we proven that the original statement is true 

### Example- proving $\sqrt2$ is irrational 

First we need by take our premise and the negation of our conclusion, i.e assuming that $\sqrt{2}$ is rational 

$$ \sqrt{2} \text{ rational } \implies \exists a,b, \in \mathbb{Z} \space s.t. a/b = \sqrt{2} $$
And now we need to show that $\exists a,b, \in \mathbb{Z}$ is false 

So suppose  $\exists a,b, \in \mathbb{Z}, \space s.t. a^2 = 2b^2$ - this is our premise 

Let $d$ be the greatest common divide of $a,b$ (definition)

Then $d$ is a divisor of $a$ and $d$ is a divisor of $b$ (by defn of g.c.d)

$\exists u \in \mathbb{Z} \space s.t. a = du$
$\exists v \in \mathbb{Z} \space s.t. b = dv$

So we have $(du)^2 = 2 (dv)^2$ (substitution)
After expanding an simplifying, we have: 
$(u^2) = 2v^2$
We’ve kind of got to where we started, but instead of having $a$ and $b$, we have $u$ and $v$, but instead this time, $u$ and $v$ cannot be even due to our introduction of the g.c.d. 

But look again at our expression, $u^2$ is even (defn of even), so $u$ is even (previous result)
Therefore, $\exists k \in \mathbb{Z} \space s.t. u = 2k$ 
So $(2k)^2 = 2v^2$ (substitution)

After some expanding and simplifying, we have that 
$(2k)^2 = v^2$ 
So this means that $v^2$ is even (by defn of even) and $v$ is even

So now $\exists l \in \mathbb{Z} \space s.t. v = 2l$

And after we substitute back into the definitions of $a$ and $b$, we get; 

$$ a = d(2k)$$$$ b = d(2l)$$ We started by assuming that $d$ was the g.c.d of $a$ and $b$, but here, $2d$ is the g.c.d 
As $d < 2d$ , $d$ is not the g.c.d of $a$ and $b$, hence, we have reached a contradiction 

If our statement $P$ was “$d$ is the g.c.d of $a$ and $b$, then $\neg P$ was $d$ is not the greatest g.c.d of $a$ and $b$. Therefore, we have $P \wedge \neg P$, which is a contradiction 

Hence, our premise is false, so $$ \forall a,b \in \mathbb{Z}, \space a^2 \neq b^2$$


---

# Integers 

**Axioms** - set of properties that we accept without requiring a proof 
How do we know that axioms are axioms? 

There is a list of **algebraic axioms** and **order axioms**: 

![Pasted image 20251015104358.jpg](/img/user/Pasted%20image%2020251015104358.jpg)

All of these axioms will hold true even if we work with the reals, naturals, and complex numbers, and that’s why we have the ordering axioms - which work for the set of integers. 

For $m, n \in \mathbb{Z}$, exactly one of the properties below hold: 
- $m < n$ 
- $m = n$ 
- $m > n$ 
We can prove the other inequalities from the properties above 
#finishexplaination - talk about how to get the other inequalities 


### Proof that $0< 1$ (proof by contradiction)

Our starting point to take the premise and negation of our conclusion as the assumption: 

So suppose $\neg(0 < 1) \implies 1 \leq 0$

The **scaling axiom** says something about 0. 

According to the shift axiom: 

$$ 1 + (-1) \leq 0 + (-1) $$
Then using the negation, and identity axiom: 
$$ 0 \leq -1$$
Scaling axiom, we can rescale by $-1$
$$ 1 (-1) \leq 0(-1) $$
And by identity axiom: 
$$ -1 \leq 0 $$This isn’t a proper contradiction, even though it may feel like one, but feelings, as we know, are not always facts. So let’s keep going 

By the Anti-symmetric condition: 

$$ 0 = -1 $$
Substitution: 
$$ 0+ 1 = - 1 + 1 $$
By identity and negation 
$$ 1 = 0$$
And by the identity axiom once again: 
$$ 1 \neq 0 $$
And hence we have contradiction 

### Note on the Well-ordering principle 
Essentially, $n$ is the least element of a set $S$ if: 
- $n \in S$ 
- $\forall m \in S, m \leq n \implies m = n$ 
This is just means that $n$ is the smallest element in the set, and if there is a smaller element $m$ than $n$, then that element just equals $n$. 

#### Proof of $1$ being the least element of the set $\mathbb{N}_1$ of positive integers 

Let $n$ be least element of $N_1$ 

We can say that

$$ 1 \leq n  \text{ and } n \leq 1$$
Assume $1 \leq n$
But as $n$ is the last element of $\mathbb{N}_1$ and $1 \in \mathbb{N}$, so $n=1$ 

Now let’s assume that $n \leq 1$. What we’re trying to show that there are no elements between $0$ and $1$ 

We know that $n \in \mathbb{N}$, so we can apply the scaling axiom to say that: 
$$ n \cdot n \leq 1 \cdot n $$
So now is $n^2 \in \mathbb{N}$? 
We can use scaling axiom to say that: 
$$ 0\cdot n \leq n \cdot n $$
By the zero divisor axiom we have that $n \cdot n = 0 \implies n=0 \text{ or } n=0$
This is a contradiction as $0 \leq n$ 

So we know that $n \cdot n \in \mathbb{N}$ 

But we know that $n$ is the lease element of $\mathbb{N}_1$ 

So $n \cdot n \leq n$ 

$$ n\cdot n + (-1) \cdot n = 1 \cdot n + (-1) \cdot n$$
$$ (n-1) \cdot n = 0 \cdot n = 0 $$
So we have 
$n \cdot 1 = 0$ or $n = 0$ 

So $n = 1$ 

## Proof by Induction 

$$ \text{ If } P(1) \land [\forall n \geq 1, P(n) \implies P(n+1)] \implies P(n) \equiv T \space \forall n \geq 1$$
- The first step is called the **base step** where use a starting case for induction 
- Second step is the **inductive step**
- The premise $P(n)$ in the inductive step is called the **inductive hypothesis**
### Proof of the proof by induction 

What we want to prove that is $P(1)$ is true, then $\forall n \geq 1, P(n) \implies P(n+1)$, then $P(n)$ is true $\forall n \geq 1$ 

And we'll prove it by contradiction. So we assume the conclusion is false, i.e. $\exists k \in \mathbb{N}_{1} \space s.t. P(n) \equiv F$

So if there exists at lease one number $k$ where $P(k)$ is false, we can collect all of them into a set: 

$$ S = \{  k \in \mathbb{Z} : k \geq 1 : P(k) \equiv F \} $$
This set $S$ is non-empty, because we're assuming that there's at least one false case 

By the W.O (well ordering) principle, every non-empty subset of $\mathbb{N}$ has a least (smallest) element, and since $S$ is non-empty, there must be a smallest number, let that number be $m$. 
This means that: 
- $P(m)$ is false as $m \in S$ 
- Every smaller number has $P(n)$ True because $m$ is the first smallest number for which $P$ fails 

Now we have a few cases to consider: 
- If $m=1$, we've contradicted the premise, which says that $P(1)$ is true, so this is a contradiction. So $m \neq 1$ 
- $P(m-1)$ is true, because $m-1 < m$ and all the numbers smaller than $m$ are true 
- The inductive steps means that if $P(n)$ is true, then $P(n+1)$ is true 

If $m$ is the smallest number where $P$ fails, then consider $n = m-1$, for which $P(n)$ is true, by the inductive step we have: 
$$ P(m-1) \implies P(m) $$
So $P(m)$ must be true, but as we've defined $m$ to be the first case where $P(m)$ is false as $m \in S$, this leads to a contradiction. 

This means there are no numbers in the $S$ which satisfy the property, so there is no point where induction fails. 

#### Example 

Suppose we want to prove that $$ \forall n \geq 1, n! \leq n^n$$
So we start with the base case, $n=1$ 

$1! =1$ and $1^1 = 1$ 

Now for the inductive step, we want to prove the statement below: 

$$ \forall n \geq 1, n! \leq n^n \implies (n+1)! \leq (n+1)^{n+1}$$
We assume the statement holds for some $n$, and this is the induction hypothesis, so assume $$ P(n) = n! \leq n^n$$
And now we want to prove this for $(n+1)$ 

$$ P(n+1)= (n+1)! \leq (n+1)^{n+1}$$
By the def. of factorial, we have 
$$ (n+1)! = (n+1) \times n!$$
Now, using our scaling axiom and the inductive hypothesis ($P(n) = n! \leq n^n$), we have: 
$$ (n+1) \times n! \leq (n+1) \times n^n$$
As we know that $n < n+1$, we have that $n^n < (n+1)^n$. Using the scaling axiom again we have:  
$$ (n+1) \times n^n < (n+1) \times (n+1)^n = (n+1)^{n+1} $$
Notice how this gives us the following: 
$$(n+1)! < (n+1)^{n+1} $$
Hence the result follows by mathematical induction 
## Weak vs Strong induction 

In weak induction, we only look one step back, i.e. assume that $P(n)$ is true and then use that to show that $P(n+1)$. 

Strong induction is slightly difference, as we assume all the past results to prove the next step in the induction step, i.e. use all $P(1), P(2), ... , P(n) \implies P(n+1)$ 

Decimal expansions, as covered in the next section, are an application of strong induction as we need the fact that every smaller number has a representation. 
### Decimal Expansions 

#finishexplaination 
## Remainder Theorem 

Useful for modular arithmetic which is useful for cryptography 

[[Tags/Definition\|Definition]] 
If $a$ and $b$ are integers with $b \neq 0$, then there is a **unique** pair of integers $q$ (quotient) and $r$ (remainder) such that $$a = qb +r , \quad 0 \leq r < |b|$$
It's $|b|$ because the absolute value makes it work whether $b$ is positive or nrgative 
Consider two cases below: 
$$  10 = 3 \times 3 + 1$$
$$  10 = 0 \times 3 + 10$$
The second case is wrong because we can still take away 3 from 10. So that’s the idea of the proof, just keep taking away from the remainder until we’re left with a negative number as the remainder must be positive 

### Proof of the remainder theorem 

The proof has few parts
- Existence - showing there are such integers $q$ and $r$ that work 
- Show that the remainder $r$ is less than $|b|$ 
- Uniqueness - showing they are the only such pair 

#### Existence 
Let's start with case 1: $a \geq 0$ 

The idea is that we keep subtracting $|b|$ from $a$ until what's less is less than $|b|$ 
Formally, we define a set: 
$$S = \{  r^` \in \mathbb{Z} : r^` \geq 0 \text{ and } \exists q^` \in \mathbb{Z}, a = q^`|b| + r^` \} $$

So $S$ is essentially the set of all non-negative remainders we can get when subtracting multiples of $|b|$ from $a$ 

Consider case 2: $a < 0$ 

If $a$ is negative, we just flip the sign: 
$$ a = q|b| + r \implies -a = (-q)|b| -r$$
So the theorem works for all $a$, positive and negative 
#### Showing  $r < |b|$ 

Notice that $S$ is non-empty as for $q=0,\quad a-0|b| = a \geq 0$ , so by the well-ordering, every non-empty set of non-negative integers has a smallest element 

Let that smallest element be $r$. 
Suppose for contradiction that $r \geq |b|$
Then we can make a new remainder: $r^` = r-|b|$ 

Notice that: 

$$a = q|b| + r = (q+1)|b| + (r-|b|) = (q+1)|b| + r^` $$
This means that $r^` = r-|b| \leq 0$, so $r^` \in S$ 

We've just shown that $r^` < r$ which leads to a contradiction as $r$ is meant to be the smallest element, so $r^` \not \in S$, which means that $r < |b|$ 
#### Uniqueness

Suppose that there were two pairs: 

$$ a = q_1|b|+ r_{1} = q_{2}|b| + r_{2}, \quad 0 \leq r_{1}, r_{2} < |b|$$
We subtract one from the other to get: 
$$ (q_{1} - q_{2})|b| = r_{2} - r_{1}$$
This means that the left side is a multiple of $b$, but the right side is smaller than $|b|$ as both remainders are between $0$ and $|b|$ 

Now, if the left side is a non-zero multiple of $b$, then its absolute value must at least be $b$, but the right side is strictly less than $b$. So the only way this equality can hold true is if the right side is $0$ 

So $r_1 = r_2$ and therefore $q_1 = q_2$ 

So the pair $(q,r)$ is unique 

# Divisibility and Euclid’s Theorem 

