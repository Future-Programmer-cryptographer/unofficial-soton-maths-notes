---
{"dg-publish":true,"permalink":"/semester-1/number-theory-i/"}
---

# Link back to [[Semester 1/Home page\|Home page]]

#   [HTML version ](https://www.southampton.ac.uk/~wright/1001/)

---
# 1. Introduction to Proofs and Logic 

[[Tags/Definition\|Definition]] A **statement** (or proposition) is an expression that can be assigned the value of true or false 

Anything that’s a question is not a statement. 
In the example below, it’s a statement as the variable is “used up”. We really need to specify what’s happening to the variable for it to be a statement.  
$$ \sum_{i=1}^{4} i=10 $$

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

And after we substitute back into the definitions of $a$ and $b$, we get:
$$ a = d(2k)$$$$ b = d(2l)$$ We started by assuming that $d$ was the g.c.d of $a$ and $b$, but here, $2d$ is the g.c.d 
As $d < 2d$ , $d$ is not the g.c.d of $a$ and $b$, hence, we have reached a contradiction 

If our statement $P$ was “$d$ is the g.c.d of $a$ and $b$, then $\neg P$ was $d$ is not the greatest g.c.d of $a$ and $b$. Therefore, we have $P \wedge \neg P$, which is a contradiction 

Hence, our premise is false, so 
$$ \forall a,b \in \mathbb{Z}, \space a^2 \neq b^2$$


---

# 2. Integers 

**Axioms** - set of properties that we accept without requiring a proof 
How do we know that axioms are axioms? 

There is a list of **algebraic axioms** and **order axioms**: 

- [Operations (Op)] The integers are equipped with two _binary operations_ addition and multiplication. These operations are denoted by the symbols $+,⋅$respectively.
- [Identity (Id)] Z contains two special elements, denoted $0$ and $1$, with $0≠1$ such that for any integer $m, m+0=0+m=m$ and $m⋅1=1⋅m=m$.
- [Negation (Neg)] For every integer $m$, there exists an integer denoted $−m$ such that $m+(−m)=(−m)+m=0.$
    We write $a−b$ as a shorthand for $a+(−b).$
- [Commutative (Comm)] Addition and multiplication are commutative, i.e. $m+n=n+m and m⋅n=n⋅m \space \forall m,n∈Z$
- [Associative (As)] Addition and multiplication are associative, i.e. $(m+n)+p=m+(n+p)$ and $m⋅(n⋅p)=(m⋅n)⋅p \space \forall m,n,p∈Z$
- [Distributive (Dist)] Multiplication distributes over addition, i.e, $m⋅(n+p)=m⋅n+m⋅p \space \forall m,n,p∈Z.$
- [Zero divisors (ZD)] If $m⋅n=0$ then $m=0$ or $n=0$.

- [Order relation (Ord)] $\mathbb{Z}$ is equipped with a relation $≤$ called “less than or equal to”.
- [Reflexive (Ref)] Every integer $m$ satisfies **$m≤m$**.
- [Antisymmetric (ASy)] Given two integers **$m,n$**,** if **$m≤n$** and **$n≤m$** then $m=n$.
- [Transitive (Tr)] If **$m,n,p$** are integers with **$m≤n$** and $n≤p$ then $m≤p$.
- [Comparability (Comp)] Given any two integers $m,n$ either $m≤n $or $n≤m$.
- [Shift (Sh)] If $m,n,p$ are integers with $m≤n$, then $m+p≤n+p$
- [Scale (Sc) ] If $m,n,p$ are integers with $m≤n $and 0≤p then $m⋅p≤n⋅p$.
- [Well ordering (WO)] The well ordering principle – any non-empty subset of non-negative integers has a unique least element.

All of these axioms will hold true even if we work with the reals, naturals, and complex numbers, and that’s why we have the ordering axioms - which work for the set of integers. 

For $m, n \in \mathbb{Z}$, exactly one of the properties below hold: 
- $m < n$ 
- $m = n$ 
- $m > n$ 
We can prove the other inequalities from the properties above 


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
It's $|b|$ because the absolute value makes it work whether $b$ is positive or negative 
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

# 3. Divisibility and Euclid’s Theorem 

[[Tags/Definition\|Definition]] An integer $d$ is a **divisor** of the integer $a$ iff there is an integer $b$ such that $db =d$

Notation - $d|a$ means $d$ is the divisor of $a$ (i.e $\frac{a}{d}$ is a integer but we’re not allowed to write it in division/fraction form)

Fun fact - not every integer is a divisor of every other integer 

## Greatest Common Divisor
[[Tags/Definition\|Definition]] The **greatest common divisor** of $a$ and $b$ is the unique integer $d$ satisfying: 
- $d|a$ and $d|b$ 
- If $c|a$ and $c|b$ then $c \leq d$ so that no common divisor exceeds $d$ 

Notation - the greatest common divisor of $a$ and $b$ is given by: $\gcd(a, b)$

## Euclidean Algorithm 

Essentially, the Euclidean Algorithm finds the gcd of two integers $a$ and $b$ 

Consider the example below: $a = 252$ and $b = 105$ 

We do repeated division: 
$$ 252 = 2 \times 105 + 42  \text{ remainder 42}$$
$$ 105 = 2 \times 42 + 21 \text{ remainder 21}$$
$$ 42 = 2 \times 21 + 0 $$
When the remainder becomes $0$, the last non-zero remainder is the greatest common divisor. Hence $\gcd(252, 105) = 21$ 

Basically, we repeatedly apply the remainder theorem on numbers and do some shifting until the remainder is 0. The proof of the Euclidean will be covered later in the module 
 
$$ a= q_0b + r_0 , \quad 0 \leq r_0 < b$$
$$ b= q_1r_0 + r_1 , \quad 0 \leq r_1 < r_0$$
$$ r_0= q_2r_1 + r_2 , \quad 0 \leq r_2 < r_1$$
$$ \cdots $$
$$ r_i = q_{i+2}r_{i+1} + r_{i+2} , \quad 0 \leq r_{i+2} < r_{i+1}$$
$$ \cdots $$
$$ r_{n-2}= q_nr_{n-1} + r_n , \quad 0 \leq r_n < r_{n-1}$$
$$ r_{n-1}= q_{n+1}r_{n} + 0 , \quad 0 \leq 0 < r_n$$

where $r_n = \gcd(a,b)$

Each line $a = qb + r$ says the same common divisor that divide $a$ and $b$ will also divide $r$. And this is where the linear combination in the section will come in. 
### Divisors and Linear Combination 

**Cancellation Lemma** - if $m,b,p \in \mathbb{Z}$ s.t. $mp \implies np$ and $p \neq 0$, then $m=n$ 

We can use this lemma and the linear combination to prove Eucledian's Algorithm 

If $a,b$ are integers with $a = qb + r$ then $\gcd(a,b) = \gcd(b,r)$

Now, if we can show that any common divisor of $(a,b)$ also divides $(b,r)$ and any common divisor of $(b,r)$ also divides $(a,b)$, this is means common divisors are the same, so their greatest common divisor must be the same, i.e. $\gcd(a,b) = \gcd(b,r)$

Let the common divisor of $(a,b)$ and $(b,r)$ be $d$. And we want to show that $d|r$ and $d|a$. It's like showing that two subsets are equal, which means they are the same set. 

So if $d|a$ and $d|b$, then $a = dk_1$ and $b = dk_2, \space k \in \mathbb{Z}$

Now, using the remainder theorem we have: 
$$ dk_{1} = q(dk_{2}) + r$$
$$ \implies dk_{1} - qdk_{2} = r$$
$$ \implies d(k_{1} - qk_{2}) = r$$
Hence $d|r$ 

Now to prove the converse - if $d|b \land d|r \implies b|a$

$b = dk_3$ and $r = dk_4 \space k \in \mathbb{Z}$ 

Using the definition again we have: 
$$ a= q(dk_{3}) + dk_{4} = d(qk_{3} + k_{4})$$
Hence, by definition, we have $d|a$ 

And therefore, $\gcd(a,b) = \gcd(b,r)$
### Proof of Euclid’s Algorithm 

The Euclid algorithm is essentially the step above repeated
$$ a = q_{1}b + r $$
$$ b = q_{2}r_{1} + r_{2} $$
$$ r_{1} = q_{3}r_{2} + r_{3} $$
$$  \dots $$
until the remainder becomes 0: 

There's a nice proof by contradiction to show that this process does not go on forever. So assume this goes on forever, then the set containing all the remainders is: $S=\{  r_{1}, r_{2}\dots r_{n} \}$ will have no least element-- which contradicts the W.O axiom, so there must be a least element, which is $r_n = 0$ 
 
By the rule, we've just proved that: 
$$ \gcd(a,b) = \gcd(b,r_{1}) = \gcd(r_{1}, r_{2}) = \dots = gcd(r_{n-1}, r_{n}) $$
So when we finally hit $r_k = 0$, the gcd is the last non-zero remainder: 
$$ \gcd(a,b) = r_{n-1}$$

## Euclid’s Algorithm for Polynomials 

The operation on polynomials satisfy all of the algebra axioms as the integers do, so they are an example of a **commutative** **ring**. But matrices are an example of non-commutative ring as they don’t saying the commutativity axiom 

[[Tags/Definition\|Definition]] A **commutative ring** is a set $R$ equipped with two binary operations: $+, \cdot$ and satisfying the axioms Op, Id, Neg, Comm, As, Dist 

## Bezout’s (Bucket) Identity 

[[Tags/Definition\|Definition]] If $a$ and $b$ are integers, then $\exists u$ and $\exists v$ s.t. 
$$ \gcd(a,b)= au+ bv $$
And then $\gcd(a,b)$ is the least positive integers of the form of $au + bv \quad (u,v) \in \mathbb{Z}$

Consider two buckets, one 4 litre and one 7 litre, now, can we measure 1 litre using those two? 
Well, fill up the 4l twice and then pour it in the 7l, whatever’s left in the 4l is 1l, and that’s what Bezout’s Identity is telling us - we can solve the bucket problem when the gcd is what we’re trying to measure. 

### Ideals 

The proof of Bezout’s Identity involves a set called **ideals**

[[Tags/Definition\|Definition]] Let $R$ be a ring, then the subset of $I$ in $R$ is an **ideal** if: 
- $I$ is non-empty 
- $\forall a,b, \in I, a+b \in I$ - closed under addition 
- $\forall a \in I$ and $r \in \mathbb{Z}, ra \in I$ - closed under multiplication by any non-negative integer  

Notice how this is similar to vector sub spaces in linear algebra. 

For example:
- The set $I = \set{0}$ is an ideal of $\mathbb{Z}$
- The set of even numbers is an ideal of $\mathbb{Z}$ 
- The set of odd numbers is not an ideal as it’s not closed under addition nor multiplication by all other integers 

**Closed** means that we don’t have to move outside the set if we apply an operation, i.e. if set $S$ has an operation $*$, then $S$ is closed under $*$ if 
$$ S_1, S_2 \implies S_1*S_2 \in S$$
### Proof of Bezout’s Identity 

**Lemma 3.14** Let $a, b \in \mathbb{Z}$, then the set: 
$$ I = \set{au +bv : u,v \in \mathbb{Z}}$$
Is an ideal in $\mathbb{Z}$ as it's is non-empty because we can have $a(1) + b(0) \in I$ and it's is closed under addition and multiplication 

Now, let $I$ be a non-zero ideal in $\mathbb{Z}$, then $\exists d\in I$ s.t.: 
**Lemma 3.15**
$$  x \in I \iff d|x$$
In other words, take any non-zero ideal $I \in \mathbb{Z}$, then $\exists d \in \mathbb{Z}$ s.t. 
- Every element of $I$ is a multiple of $d$
- Every multiple of $d$ is in $I$
- Among all the elements of $I$, $d$ is the smallest 

This means $I$ has the form: 
$$ I = \set{nd: n \in \mathbb{Z}} $$

What this basically means is that every ideal in $\mathbb{Z}$ is made of all the multiples of one single number. And that one number is the smallest positive element in that ideal. 
Why do we care? Because Bezout's identity is about showing that the $\gcd$ of this idea is the smallest positive element in that ideal. In other words, for any ideal $I \in \mathbb{Z}$, when we input the ideal of all linear combinations $a,b$, the the output $d$ gives us exactly $\gcd(a,b)$ -- which is very cool!! 

So we let $d$ be the least positive element of $I$ (W.O principle)

Now we want to show for the iff that:
1. $x \in I \implies d|x$ 
2. $d|x \implies x \in I$ 

2.Suppose $d|x$
$\implies \exists q \in \mathbb{Z} \space s.t. \quad x = qd$ 
$d \in I$ by definition 
$q \in \mathbb{Z}$ 
$I$ is an ideal 
So $x =  q \cdot d \in I$ because by definition an ideal is closed under multiplication by any integer, all multiples of $d \in I$

1. Let $x \in I$
Then by the remainder theorem we have $x = qd + r \quad q,r \in \mathbb{Z} \quad 0 \leq r < |d|$
We know that $d \in I \implies (-q)d \in I$  as by definition, multiplies of $d$ are in $I$ as ideal is closed under multiplication 

Now, $r = x - qd = x + (-q)d$ 
as $x \in I$ and $(-q)d \in I$ $\implies$ $x   + (-q)d \in I \implies r \in I$ 
As $r < d$ by definition of the remainder theorem, and $d$ is the least a positive positive element of $I$, $r$ is not positive $\implies r \leq 0$, but as we have that $r > 0 \implies r = 0$ 

Hence, we have shown that $x = qd + 0 = qd$, so every element of $I$ is in fact a multiple of $d$ 

Now, all that remains is to show that $d$ is the $\gcd(a,b)$ 

So let: 
$$  I = \{  au + bv : u,v \in \mathbb{Z} \}$$
This is an ideal by Lemma 3.14, and so by Lemma 3.15, $\exists d \in I$ s.t. $d|x \space \forall x \in I$ 

Since $d \in I$, by definition, $\exists u,v$ s.t. $d = au + bv$ 

Now, we want to show that $d$ divides both $a$ and $b$. 
Note that both $a$ and $b$ are in $I$, so: 
- $a = a \cdot 1 + b \cdot 0 \space \in I$ 
- $b = a \cdot 0 + b \cdot 1 \space \in I$ 

Therefore, $d$ is a common divisor of $(a,b)$ 

Let $c$ be any common divisor of $(a,b)$ 
- If $c|a$ and $c|b$, then $c$ divides any combination of $au + bv$ 
- So $c$ divides element of $I$ and in particular, $c$ divides $d$ 

So any common divisor of $c$ of $(a,b)$ satisfies: 
$$ c|d \implies |c| \leq |d| $$
This means that $d$ is at least as big as any other common divisor, but since $d$ is positive, we have: 
$$ c \leq |c| \leq d $$
Therefore, $d = \gcd(a,b)$ 
$$ \square $$

## Lamé’s Theorem 

[[Tags/Definition\|Definition]]
The number of steps in the Euclidean algorithm does not exceed 5 times the number of decimal digits in the smaller of the two numbers. 

Eg: if we apply the Eucledian algorithm to integers with 100 digits, then we require no more than 500 steps in the algorithm. 

The proof of this beautifully involves the Fibonacci and the golden ratio. 

## Co-prime integers 

[[Tags/Definition\|Definition]] Two integers $a$ and $b$ are **co-prime** if $\gcd(a,b) = 1$ 

[[Tags/Definition\|Definition]] Integers $a_1, a_2,… , a_n$ are **mutually co-prime** if $\gcd(a_i, a_j) = 1, \quad i \neq j$ 

Eg: integers $6,10,15$ are co-prime but not mutually co-prime 

Two integers are co-prime $\iff$ $\exists x, y \space s.t. \space ax + by = 1$ 

If $\gcd(a,b) = d$, then 
$$ \gcd(ma,mb) = md \quad \forall m > 0 \quad \gcd(u,v) = 1$$
Where $a = ud$ and $b = vd$ 

Let $a$ and $b$ be co-prime, then: 

$$  a|c \land b | c \implies ab|c$$
$$ a|bc \implies a|c $$
Note how this only works if the numbers are co-prime. The proof of both of them are in in notes. 

## Least Common Multiple 

Pretty much self-explanatory, the lowest common multiple of two numbers is just the product of those numbers divided by the greatest common divisors of two numbers 
If $a,b \in \mathbb{Z}$ and if $d = \gcd(a,b)$ and $l =lcm(a,b)$ . Then: 
$$ dl = ab \equiv l = \frac{ab}{\gcd(a,b)} $$

## Linear Diophantine Equations 

Let $a,b,c \in \mathbb{Z}$ and $a,b \neq 0$, let $d = \gcd(a,b)$. Then the equation 
$$ ax + by = c $$
Has integer solutions $\iff \gcd(a,b) | c$ and if it does, then there are infinitely many solutions: 
$$ x= x _0 + qn, \quad y = y_0 - pn \quad (n \in \mathbb{Z}) $$
Where $a = pd, b = qd$ and $(x_0, y_0)$ is any particular solutions. It’s a bit like doing differential equations. 

### Proof 
The if an only if part is just Bezout’s identity. Any common divisor of $a$ and $b$ divides every intger linear combination of $a$ and $b$ 

So now we just need to prove what the general solution looks like 

So assume we have one particular solution, so let $(x_0, y_0)$ satisfy $ax_0 + by_0 =c$. And now we want to find out all the other pairs ($x,y$) that also make $ax + by = c$ 

Let $n \in \mathbb{Z}$ s..t 
$$  x = x_0 + qn , \quad y = y_0 - pn$$
Where $a = pd$ and $b = qd$ 

Now we put this in the $ax + by = c$ to get: 
$$ a(x_0 + qn) + b(y_0 - pn) = ax_0 + by_0 +aqn - bpn = c + d(pq-qp)n = c $$
So this works for any integer $n$ 

Now we need to show that these two are the only solutions, so we suppose that ($x,y$) is any integer solutions

We subtract the two equations to get: 
$$a (x-x_0) + b(y - y_0) = 0  $$
After substituting $a = pd$ and $b = qd$ we get: 
$$pd(x- x_0)  + qd(y - y _0) = 0 $$
After dividing through by $d$ (the cancellation lemma), we have: 
$$p (x - x_0) = -q(y - y_0) $$
What this tells us that the difference between any two solutions is related by $p$ and $q$. And since $p$ and $q$ are co-prime, because that’s what happens when we divide by the gcd, the only way this equality holds in integers is if: 
$$ x - x_0 = qn , \quad y - y_0 = -pn , \quad n \in \mathbb{Z}$$
Which is exactly the formula for the infinitely many solutions 
# 4. Prime Numbers 

[[Tags/Definition\|Definition]] An integer $p >1$ is **irreducible** if the only positive divisors of $p$ are $1$ and itself 

[[Tags/Definition\|Definition]] An integer $p > 1$ is **prime** if $\forall a,b \in \mathbb{Z}$, whenever $p|ab$ either $p|a$ or $p|b$ 

For example, to prove that $2$ is a prime number, we need to show that $2|ab \implies 2|a$ or $2|b$ 

By the remainder theorem, $\exists q_i r_i \ s.t. \ a = 2q_1 + r_1, \ b = 2q_2 + r_2, 0 \leq r < 2$ 

So we have: 
$$ab = (2q_{1} + r_{1})(2q_{2} + r_{2}) = 2(2q_{1}q_{2} + q_{1}r_{2} + r_{1}q_{2}) + r_{1}r_{2} $$
We also know that $ab$ is even, so $ab = 2k +0$ 
As the remainder theorem only gives unique values: 
$$ r_{1}r_{2} = 0 \implies r_{1} = 0 \text{ or } r_{2} = 0 \text{ by Z.D} \implies 2|a \implies 2|b$$
Therefore, $2$ is a prime number 
## Primes and Irreducible 

Prime and irreducible really mean the same thing, at least for the integers. 

Fermat was said to be confused about this difference too. If factorisation of irreducible numbers was unique, then Fermat’s last Theorem would’ve been a lot easier (why?) In other things however, this is not always true. For instance, consider the ring: 
$$ R = \{ a+ b \sqrt{ 5 } , \quad a,b,\in \mathbb{Z}\}$$
Now, I hope we can agree that 
$$ 2| 4 = (\sqrt{ 5 }+1)(\sqrt{ 5 }-1)$$
But $2$ does not divide $\sqrt{5} + 1$, so by definition of a prime, $2$ is not prime 

####  prime $\implies$ irreducible: 

Assume $p$ is prime and $p = ab, b > 0$ (premise)
By definition, $p|a$ or $p|b$. 
WLOG (without loss of generality), assume that $a = pk, k \in \mathbb{Z}$ Then: 
$$ p = ab = pk(b) = p(kb)$$
By the cancellation lemma, we have $1 = kb$ so $b \leq 1$. But as $b> 0 \implies b = 1 \implies a = p$. Therefore, $1,p$ are the only positive divisors of $p$, so $p$ is irreducible 

#### Irreducible $\implies$ prime

Note that this is not always true, as with our example in the ring, but in integers, this will work 
So let $p$ be irreducible and suppose $p|ab$. Then we want to show that $p|a$ or $p|b$ 

As $p$ is irreducible and since $\gcd(a,p)$ is a positive divisor of $p$, then $\gcd(a,p)$ must be $1$ or $p$ 

If the $\gcd(a,p) = p$, then as $\gcd(a,p)$ also divides $a$, it follows that $p|a$ 

On the other hand if the $\gcd(a,p) = 1$, then by definition $a$ and $p$ are co-prime and by Bezout's identity, we have that: 
$$ 1 = px + ay $$
Multiplying the entire equation by $b$ we have: 
$$  b = pbx + aby $$
By our assumption, as $p|ab \implies p|aby$ and $p|abx$. Therefore the RHS is divisible by $p$ and therefore $p|b$ 

Lemma 4.4: If $p$ is prime and $p|a_1, … a_k \implies p |a_i$ for some $i$ - this can be proved by induction, which is in the notes 

## The Fundamental Theorem of Arithmetic 

Each integer $n > 1$ has prime-power factorisation: 
$$ n = p_1^{e_1} … p_k^{e_k} $$
Where $p_1, … , p_k$ are distinct primes and $e_1, … e_k$ are positive integers. The factorisation is **unique**, apart from permutation of the factors 

Say I wrote a prime factorisation of $12$, how can I know that the prime factorisation is unique? That's exactly what the fundamental theorem of arithmetic allows us to do - every integer $n > 1$ is can be written as a product of primes, and this factorisation is unique up to reordering. 

The proof of this has two parts: 
- Existence - every integer has a prime-power factorisation 
- Uniqueness - this factorisation is the only one 

### Existence - using strong induction 

Base case: $n = 2$. We proved earlier that $2$ is prime, so its factorisation is simply: $2 = 2^1$ 

Induction hypothesis: assume every integer strictly between $1$ and $n$ already has a prime-power factorisation. 

Inductive step: prove it for $n$. There are two cases here: 

1 - $n$ is prime, which case $n = n^1$ and we're done 
2 - $n$ is composite 

In case 2, let $n = ab, \quad 1 < a,b < n$ 

Now both $a,b$ have prime power decomposition by the induction hypothesis, so by substituting these into the equation $n=ab$, and then collecting powers of each prime $p_i$, we get a prime-power factorisation for $n$ 
### Uniqueness 

This will also be done by strong induction. 

Base case: Suppose $n=2$ has factorisation $2 = p_{1}^{e_{1}}p_{2}^{e_{2}}\dots p_{k}^{e_{k}}$ 

Then by definition each prime $p_i \geq 2$. If there is any prime $p_1 > 2$ contradicts $p_{1}^{e_{1}}p_{2}^{e_{2}}\dots p_{k}^{e_{k}} = 2$ 
Hence the only factorisation of $2$ is $2^1$ 

Induction step: assume that $n> 2$ and that for every integer strictly between $1$ and $n$ has a unique prime factorisation up to ordering 

Now suppose we had two different factorisation: 
$$ n = p_{1}^{e_{1}}p_{2}^{e_{2}}\dots p_{k}^{e_{k}} = q_{1}^{f_{1}}q_{2}^{f_{2}}\dots q_{l}^{f_{l}}$$
Where all $p_i$ and $q_i$ are primes. Then our aim to show that these two sets of distinct primes are the same, up to reordering 

From the first factorisation, we have that: $p_1|n$ 
So in the second factorisation, by Lemma 4.4 earlier, we know that: 
$$ p_{1} |q_{1}^{f_{1}}q_{2}^{f_{2}}\dots q_{l}^{f_{l}} $$
Since $p_1$ is prime, it must divide one of the $q_j$, but each $q_j$ is prime too. So the only possibility is that: $p_1 = q_j$ 

This essentially allows us to match up one prime from each factorisation. WLOG, we can order the primes so that: $p_1 = q_1$

Now we have that 
$$p_{1}^{e_{1}}p_{2}^{e_{2}}\dots p_{k}^{e_{k}} = q_{1}^{f_{1}}q_{2}^{f_{2}}\dots q_{l}^{f_{l}} $$
We can cancel $p_1 = q_1$ from both sides to get: 
$$p_{1}^{e_{1}-1}p_{2}^{e_{2}}\dots p_{k}^{e_{k}} =q_{1}^{f_{1}-1}q_{2}^{f_{2}}\dots q_{l}^{f_{l}} $$
And this new number is strictly smaller than $n$. 

If this new number is $1$, the $k = l = 1, e_1 = f_1, p_1 = q_1$, so the two factorisation were the same. 

Otherwise, $p_{1}^{e_{1}-1}p_{2}^{e_{2}}\dots p_{k}^{e_{k}}$ is strictly between $1$ and $n$ so by the induction hypothesis, it has a unique prime factorisation up to reordering. So $k = l, e_1 - 1 = f_1 - 1$ and $p_{2}^{e_{2}}\dots p_{k}^{e_{k}} = q_{2}^{f_{2}}\dots q_{l}^{f_{l}}$ up to reordering. 

Hence by induction, this holds $\forall n > 1$ 

We can how take this theorem and show that if a positive integer $n$ is not a perfect square, then $\sqrt{n}$ is irrational, i.e. if $n$ is not a perfect square, then there are no non-zero integers s.t. $b^2n = a^2$ 
This can be done by a proof by contrapositive, look at the notes for this. 

## Distribution of Primes 

### Euclid’s Proof of Infinitely Many Primes 

Our strategy here is fairly simple: 
- Assume that we have a finite number of primes 
- Use them to build a new prime number that cannot be divisible by any of them 
- So we've missed at least one prime 
- Therefore, there must be infinitely many 

Assume we have all the primes are: 
$$ p_{1}, p_{2}, \dots p_{k}$$
Now we define a new number: 
$$ N = p_{1}p_{2}\dots p_{k} + 1 $$
Now we look at the product of the primes in $N$. We can notice that every prime $p_i$ divides that product, but $N$ is exactly $1$ more than the product of all the primes. 

So none of the primes $p_1 ... p_k$ divide $N$ 

By the fundamental theorem of arithmetic that we proved earlier, every integer has a unique prime factorisation, so $N$ must have at least one prime divisor, say $q$ 

But since none of the primes in our list can divide $N$, this new prime $q$ cannot be one of the primes in $p_1, ... p_k$, therefore $q$ is another prime, which contradicts the assumption that we had all the primes 

### Estimating Distributions 

I won't go into a lot of detail for this section, mostly because it's explained in the notes, but there are few decent, and not so decent, ways of estimating primes which can be proved by strong induction.

A very weak estimation is given by: 
$$ \text{ The } n \text{th prime } p_{n} \text{ satisfies } p_{n} \leq 2^{2^{n-1}} \ \ \forall n \geq 1 $$

The **Prime Number Theorem** however, is more of the interesting side of things, which uses this function: 
$$ \text{ li } x = \int_{2}^x \frac{dt}{\ln t}$$
It tells us how the proportion of primes goes, something else which might be of interest is to look up **Skewe's number**

# 5. Congruences 

Fun fact: a perfect square must leave a remainder $0$ or $1$ when divided by $4$ 

[[Tags/Definition\|Definition]] Let $n$ be a positive integer, and let $a$ and $b$ any integers, we say that $a$ is **congruent** to $b\mod n$ written as: 
$$  a \equiv b \mod n$$
If $a$ and $b$ leave the same remainder when divided by $n$, then the remainder if the **residue** of $a$ (or $b$) module $n$ And the number $n$ is the **modulus** 

There is more than one way to think about congruence, the following are equivalent: 

What the above essentially means is that is a divide $a$ or $b$ by $n$, then both of those remainders are the same. So $a = q_1 n + r$ and $b = q_2 n + r$ and when we rearrange, we get: $a = b + (q_1 - q_2)n$ 
$$  a \equiv b \mod n \iff \exists k \in \mathbb{Z} \ s.t. \ a = b + kn $$
Proving the next statement is just a rearrange to get: $(a-b) = kn$ which is the same as: 
$$ a \equiv b \mod n \iff  n | (a-b) $$
so $a \equiv b \mod 2$ means both $a$ and $b$ have the same parity, either they’re both even or both odd 

The properties of reflexive, symmetric and transitivity can also be seen for congruence: 
$$a \equiv a \ \forall a \in \mathbb{Z} $$
$$a \equiv b \implies b \equiv a $$
$$ a \equiv b \land b \equiv c \implies a \equiv c  $$
## Modular Arithmetic 

We can also think of modular arithmetic as the arithmetic in the quotient ring $\mathbb{Z} / (n)$. It's like all the numbers that differ by a multiple of $n$ where $n$ is the ideal $(n) = \set{ nk: k \in \mathbb{Z}}$

Another intuition is to think of digits in base $n$, so working on $\mod 7$ is like throwing away full multiples of $7$ and only taking the last digit. 

### Arithmetic of Congruences 

For any $n \geq 1$, if $a \equiv b \mod n \ \land u \equiv v \mod n$: 
$$ a + b  \equiv u + v \mod n $$
$$ ab \equiv uv \mod n $$
Now, if $a \equiv b \mod n$ and $i \in \mathbb{N}_0$, then 
$$ a^i \equiv b^i \mod n $$
However, it’s important to note that if $a,b \in \mathbb{Z}$ and $i \equiv j \mod n$, then:
$$ a^i \not \equiv a^j \mod n $$
A simple example is that, $2^1 \not \equiv 2^{10} \mod 9$ even though $1 \equiv 10 \mod 9$

#### Cancelling factors in congruences 

Suppose $ax \equiv ay \mod n$ 

Now, we want to cancel out $a$, but can we do that? By using another equivalent definition we get that: 
$$ ax \equiv ay \mod n \iff n |a(x-y)$$
Now, cancellation is allowed $\iff \gcd(a,n) = 1$, i.e. $a,n$ are co-prime. This is because then the only way for $n$ to divide $a(x-y)$ is for it to divide $(x-y) \implies x \equiv y \mod n$

Once again, notice the pattern, happens to links back to primes and composites and irreducibility 

### Multiplicative Inverses 

[[Tags/Definition\|Definition]] 

A **multiplicative inverse** modulo $n$ for a number $a \in \mathbb{Z}$ is a number $x \in \mathbb{Z}$ s.t. $ax \equiv 1\mod n$ 

And this inverse exists $\iff$ $\gcd(a,n) = 1$ 

We can notice that this comes directly from Bezout's Identity, as if $\gcd(a,n) = 1$, then $\exists x,y \in \mathbb{Z}$ s.t. $ax + ny = 1$

And now if we take this $\mod n$ we have $ax \equiv 1 \mod n$. So $x$ is the inverse of $a$ modulo $n$ 
### Divisibility 

If one number divides another, then we can say that: 
$$n |m \iff m \equiv 0 \mod n$$
So if $n$ divides $m$, then $m$ leaves remainder $0$ when divided by $n$ 

For example, consider want to prove that $6 | a(a+1)(2a+1)$ 
We can use the fact above to rewrite this as: 
 $$a(a+1)(2a+1) \equiv 0 \mod 6$$
 Now, instead of trying to expand the expression, we can see that integer is congruent to one of $0,1,2,3,4,5 \mod 6$, i.e. $a \equiv 0, 1,2,3,4,5 \mod 6$. It's like the remainder theorem. So by checking those $6$ cases proves the statement for all integers 

Another example is suppose we want to show that: 
$$a^2 \equiv a \mod 2$$
Now we don't need to test this for all the integers, all we need to do is test this for $a = 0,1$ and we're done. Because when we divide by $2$, we only have $2$ possible remainders. 

So to prove something for all integers, we can only check for possible remainders, because modulo $n$ every integer behaves like its remainder. 

**Theorem 5.17** 
If $p$ and $q$ are co-prime, then $a,b \in \mathbb{Z}$, 
$$a \equiv b \mod (p1) \iff a \equiv b \mod(p) \land a \equiv b \mod (q) $$
What this basically means is that to check divisibility by $pq$, it's enough to check divisibility by $p$ and $q$ when $p$ and $q$ are co-prime. And so with our previous example, we can say that: 
$$ 6 |a(a+1)(2a+1) \iff 2 | a(a+1)(2a+1) \land 3 | a(a+1)(2a+1) $$
This works as $2,3$ are co-prime 

## Residues 

[[Tags/Definition\|Definition]]

#finishexplaination

Consider cases for odd and even #finishexplaination 

absolute vs non-positive residues #finishexplainationi

## Polynomials over $\mathbb{Z}_n$ 

Lemma 5.23 
#finishexplaination

### Showing that a polynomial has no integer roots 
#finishexplaination 

## Congruence Classes 
[[Tags/Definition\|Definition]]

#finishexplainationi

Using the property of equalities, we define an **equivalence relation** if: 
- Reflexrive 
- Symmertric 
- Transititve 
#finishexplaination
### Equivalence class 
#finishexplainationi

Lemma 5.29 

**Partition** 
#finishexplaination 

#### Set of Congruence classes 