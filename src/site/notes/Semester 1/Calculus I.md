---
{"dg-publish":true,"permalink":"/semester-1/calculus-i/"}
---

# Link back to [[Semester 1/Home page\|Home page]]
# [Link to typed notes: ](https://blackboard.soton.ac.uk/ultra/courses/_233978_1/outline/edit/document/_7502405_1?courseId=_233978_1&view=content&state=view)

# 1. Functions 

[[Tags/Definition\|Definition]].: 
$$ f: X \rightarrow Y \text{ between sets } X \text{{ and }} Y \text{ is a map that sends each element of X to a unique element in Y}$$
Given a function 
$$ f: X \rightarrow Y $$
The **Domain** of $f$ is $X$ 
The **Range** of $f$ is the subset $R$ of $Y$ containing of $Y$ containing all elements $f(x)$: 
$$ R = \{  f(x) \mid x \in X \}$$

### Notation on intervals 
For $a<b \in \mathbb{R}$, write $[a,b]$ for the **closed interval** from $a$ to $b$, and write $(a.b)$ for the **open interval** from $a$ to $b$  

$$ [a,b] = \{  x \in \mathbb{R} | a \leq x \leq b \}$$
$$ (a,b) = \{  x \in \mathbb{R} | a < x < b \}$$
$$ [a,b) = \{  x \in \mathbb{R} | a \leq x < b \}$$
$$ (a,b] = \{  x \in \mathbb{R} | a < x \leq b \}$$



## Special functions 

[[Tags/Definition\|Definition]]

- **Injection - basically a one-to-one function** 
	- Horizontal line test 
- **Surjection** - if the range matches the “Target set” 
- **Bijection** - if a function is **both** injecetive and surjective 
	- **Inverse** functions can only exist when there is a bijection 
	- Functions need to be one to one - so injective 
	- 
- **Proper subset ($\subset$)** - Every element of $A$ is also in $B$ but not equal to $B$
- **Subset ($\subseteq$**) - Set $A$ is a subset of $B$ if every element of $A$ is also in $B$

## Proving bijection and finding inverses of functions 

1. Specify domain and codomain 

Eg: $f:\mathbb{R} \rightarrow \mathbb{R}$

$f(x) = 2x+1$

2. First, we need to show that this is an injective function 

We need to show: if $f(x_1) = f(x_2)$ then $x_1 = x_2$

$f(x_1) = f(x_2)$
$2x_1 + 1 = 2x_2 + 1$
$2x_1 = 2x_2$
$x_1= x_2$

Therefore, $f$ is injective 


3. Next, we need to prove that it's a surjective 


We need to show that: $\forall y \in \mathbb{R}, \exists x$  such that $f(x) = y$

- What this basically means is that we want to pick an arbitrary $y$ in the codomain (target set)
- Then, we want to show that we can find some input $x$ in the domain such that $f(x) = y$
- It’s essentially answering the question: **"Given an output $y$ , which input $x$ produces it?"**
- And if we can always find an $x$ and it lies in that domain, then we've covered every single $y$ 

Let $y \in \mathbb{R}$

We want to solve $f(x) =y$ to find the input $x$

$$y = 2x+1 \implies x = \frac{y-1}{2}$$
Since $\frac{y-1}{2} \in \mathbb{R}$, such an $x$ always exists. 

Therefore, $f$ is surjective 

Since $f$ is both injective and surjective, it is bijective 

## Inverse functions 

Inverse functions only exist if a function $f$ is bijective
Let $f: X \rightarrow Y$ be a function 
- The inverse function should "undo" $f$

So $f(f^{-1}(y)) = y, \space \forall y \in Y$ and $f(f^{-1}(x)) = x, \space \forall x \in X$

And it must: 
- Cover all of $Y$ otherwise $f^{-1}$ isn't defined everywhere (so a subset $\subseteq$)
- Map back to exactly one $x$ or else it wouldn't be a function

We say $g: Y \rightarrow X$ is the inverse of $f$ if: 

$$ f \circ g = I_{Y} $$ 
$$ g \circ f = I_{X}$$
This means: 

$\forall y \in Y: f(g(y)) = y$
$\forall x \in X : g(f(x)) = x$

[[Tags/Definition\|Definition]] And $I$ is the identity function
We then write $g = f^{-1}$

We can restrict the domain and range of functions (eg: trig function) to find them an inverse

$f: \mathbb{R} \rightarrow \mathbb{R}, f(x) = \sin(x)$ is not a bijection 

But… $f: [\frac{-\pi}{2}, \frac{\pi}{2}] \rightarrow [-1,1], f(x) = \sin(x)$ is a bijection so an inverse does exist

## Exponentials And logs 

[[Tags/Definition\|Definition]] of exponential 
$$f: \mathbb{R} \rightarrow (0,\infty), f(x) = a^x$$

Properties: 

![Pasted image 20251001112108.png](/img/user/Pasted%20image%2020251001112108.png)

$a^x$ is also a bijection so it has an inverse function 

[[Tags/Definition\|Definition]] The **logarithm** with base a is the function: 
$$ \log_a  : (0,\infty) \rightarrow \mathbb{R}$$
Defined by $log_a(x) = y$ iff $a^y = x$

$$ log_a(a^x) = x $$
$$ a^{log_ax} = x  $$


Properties: 
![Pasted image 20251001112026.png](/img/user/Pasted%20image%2020251001112026.png)

### Proof for property 4- power property

$$ \log_a{x^y} = y \log _{a} x$$
Let $c$= $log_{a}x$
Then $x = a^c$
Raise both sides to the power of $y$ 
$$x^y=(a^c)^y$$
Take logs of both sides we have.. 
$$ \log_{a}x^y = \log_{a}a^{cy} $$ 
Simplify.. 
 $$ \log_{a} x^y = cy $$ 
 Substitute back in for $c$ we have 
$$ \log_{a}x^y = y \log_{a}x$$




## Even functions 
[[Tags/Definition\|Definition]] A function is even if: 

$$f(-x) = f(x) , \forall x \in f $$
- Symmetric about the y-axis 
## Odd function 

[[Tags/Definition\|Definition]] A function is odd if: 
$$ f(-x) = -f(x) , \forall x \in f$$
- Symmetric about the origin 


---
# 2. Limits 

## Informal intuition 

Informally, $$\lim_{x \to a} f(x) = L $$ if $f(x)$ approaches $L$ as $x$ approaches $a$ 

- Limits don’t care about what happens when when $x=a$, it just cares about what happens when $x$ is approaching $a$ 

## Formal definition

[[Tags/Definition\|Definition]] 

Let $I$ be the open interval containing $a$, and let $f$ be a function defined on $I$, except maybe not at $a$. The limit of $f(x)$, as $x$ approaches $c$ is $L$, given by: 
$$ \lim_{ x \to a} f(x)= L \iff \forall  \epsilon > 0, \space \exists \delta > 0 \space s.t. \space 0 < |x-a| < \delta \implies |f(x) - L| < \epsilon $$
The definition above reads, for any given $\epsilon > 0$, there exists $\delta >0$ such that for all $x \neq a$, if $x$ is within $\delta$ units of $a$ but not exactly equal to $a$ (limits describe approaching a point), then, $f(x)$ will be close enough to $L$ within $\epsilon$ 

Note the order in which $\epsilon$ and $\delta$ are given. Think of $\epsilon$ as the $y$-tolerance and then the limit will exist if we can find an $x$-tolerance $\delta$ that works.

For some intuition, think of it this way: 
- Someone gives you an $\epsilon$, - how close they want the output to $L$
- We then respond with a $\delta$, - how close the input must to be $a$ 
	- We want to imagine shrinking the range of inputs, then see if the range of outputs narrows down to a specific value
- And then we just have to make sure that we can respond with a $\delta$ for every single $\epsilon$ given to us

If we cannot find a value for $\epsilon$ for which there is no corresponding $\delta$, then the limit does not exist 

### Example proof: 

- We need to have a relationship between $\epsilon$ and $\delta$ to use them in a proof 

Consider the claim: $\lim_{x \to 2} (2x +1) = 5$

First, we must determine a value for $\delta$ to work with. To find that, we begin with the final statement in our proof and work backwards: 

$$| f(x) - L | < \epsilon$$
$$| (2x+1) - 5 | < \epsilon$$
$$| 2x - 4 | < \epsilon $$
We can factor out the 2 to get: 
$$ 2 |x-2|  < \epsilon $$
As we want this to be $< \epsilon$, this will only be true if: 
$$| x-2 | < \frac{\epsilon}{2}$$
$$| x - a | < \delta \implies \delta = \frac{\epsilon}{2}$$
Now that we have a value for $\delta$, we can begin our proof 

Our goal is to show that for every $\epsilon > 0$, there exists a $\delta > 0$, such that if $0<|x-2| < \delta$, then $|(2x+1) -5 | < \epsilon$

Suppose $\epsilon > 0$ has been provided 
We then define $\delta = \epsilon/2$
Since $\epsilon > 0$, we have $\delta > 0$ 

By starting with the assumption, we have $$0 < | x -2 | < \delta$$
Then after substutiting in for $\delta$
$$ 0 < | x -2 | < \frac{\epsilon}{2}$$
Then multiply both sides by 2: $$2|x-2| < \epsilon$$
But we know that $$2|x-2| = |f(x) - L|$$
So we have shown that:$$ |f(x) - L | < \epsilon $$

## Properties of Limits 

### The triangle inequality 

$a, b,c \in \mathbb{R}$  
$$|a+b| \leq |a| + |b|$$
The proof of the inequality below is covered in Linear Algebra I which uses the Cauchy-Schwarz theorem. 
$$|a-b| \leq |a-c| + |c-b|$$

To think of this intuitively, the magnitude of the sum is always less than the sum of the magnitudes. In terms of vectors, a direct path is always shorter than going to and back. 

### Uniqueness of limits + proof

$$ \lim_{x \to a} f(x) = L \text{ and } \lim_{x \to a} f(x) = M \implies L = M $$

We're essentially trying to show that a function cannot have two difference limits at the same point. So the goal is to prove that if a limit exists, it's unique 

If $f(x)$ is within an $\epsilon$ band of $L$, and also within an $\epsilon$ band on $M$ , then those bands must overlap, and therefore $L$ must equal $M$. 

#### Proof strategy (in words):
To show that $L = M$, we want to prove that the distance between those two is, $|L-M| < \epsilon, \space \forall \epsilon > 0$

- The idea here to assume that $L \neq M$ 
- And then pick an $\epsilon$ that separates them
- We then use the definition of limit to find two $\delta$ conditions 
- We show that they can't both be true for the same $x$
- Conclude that $L =M$


#### Proof - the epsilon-delta version 
So, if the limits $L \neq M$, that means there is some positive distance $d$ that separates them: 

$$d = |L - M | > 0$$
Next, we want to pick an $\epsilon$ that creates a gap between those intervals that don't overlap as that's the only way we have have $f(x)$ not lying in both intervals. 
$$\epsilon = \frac{d}{2} = \frac{|L-M|}{2}$$
And now we can use the definition of limit 
For the first limit, we have: 

$$\lim_{x \to a} f(x) = L \implies \forall \epsilon > 0, \exists \delta_1 > 0 \space s.t. \space 0 < |x-a| < \delta_1 \implies |f(x) -L | < \epsilon $$

And for the second limit: 
$$\lim_{x \to a} f(x) = M \implies \forall \epsilon > 0, \exists \delta_2 > 0 \space s.t. \space 0 < |x-a| < \delta_2 \implies |f(x) -M | < \epsilon $$
Now, we take $\delta$ to be the smaller of the two so that we can have an $x$ that is inside both $\delta$ intervals 
 $$\delta = min(\delta_1, \delta_2)$$

That means that whenever $0< |x-a| < \delta$, both conditions hold at once. So for any $x$ close enough to $a$, $f(x)$ is within $\epsilon$ of both $L$ and $M$. 

By definition of a limit, if $L$ and $M$ both exist, then when $x$ is close enough to $a$, $f(x)$ must be close enough to both $L$ and $M$. So we're looking for any $x$ close that is enough to $a$, so that $f(x)$ is within $\epsilon$ of both $L$ and $M$. 

So $|f(x) - L| < \epsilon$ and $|f(x) - M| < \epsilon$

And now we can use the triangle inequality, but we we add and subtract $f(x)$. We want to go from something we know about $f(x)$ and to something relating to the distance between $L$ and $M$. 

$$|L-M| = | L - f(x) + f(x) - M| $$
And by the triangle inequality: 
$$|L - M | \leq | L - f(x)| + | f(x) - M |$$
Given what we already know about those terms: 
$$|L - M | < \epsilon + \epsilon = 2\epsilon$$

Given our chose of $\epsilon$ above, we have: 

$$|L - M | < 2 \epsilon $$

$$| L - M | < 2 \times \frac{|L - M |}{2} $$

But this is a a contradiction as we can't have a number that's strictly less than itself, and this means our assumption $L \neq M$ was wrong, and therefore $L = M$ 

### Arithmetic of Limits 

Suppose that $\lim_{x \to a} f(x) = L$ and $\lim_{x \to a} g(x) = M$, then the following properties hold 

$$\lim_{x \to a} (f(x) + g(x) ) = L + M $$
$$\lim_{x \to a} (f(x) - g(x) ) = L - M$$
$$\lim_{x \to a} f(x)g(x) = LM$$$$\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{L}{M}, \space M \neq 0 $$
$$ \lim_{x \to a} c f(x) = cL $$
$$ f(x) \leq g(x) \text{ near a} \implies L \leq M$$


#### Proof for the sum of limits 

Given $\lim_{x \to a} f(x) = L,$ we know that 

$$\forall \epsilon > 0, \exists \delta_1 > 0 s.t. 0 < | x - a | < \delta_1 \implies |f(x) - L | < \epsilon$$

And given the other limit, we also know that: 

$$\forall \epsilon > 0, \exists \delta_1 > 0 s.t. 0 < | x - a | < \delta_2 \implies |f(x) - M | < \epsilon$$
This proof will we very similar to the uniqueness of limits in terms of algebraic manipulation. So once again we pick $\delta=min(\delta_1, \delta_2)$

What we're trying to prove is $\lim_{x \to a} (f(x) + g(x) ) = L + M$, in other words, $f(x) + g(x)$ is really close to $L+M$, so the distance between them is really small, some value smaller than $\epsilon$, so the below expression is what we're trying to prove: 
$$| f(x) + g(x) - (L+M) | < \epsilon $$
We can't control $f(x) + g(x)$ as a while, but we can control how far $f(x)$ is from $L$ and how far $g(x)$ is from $M$. So we rewrite the expression to get: 
$$| f(x) + g(x) - (L+M) | = | (f(x) -L) +  (g(x) - M) | $$
And now we can apply the triangle inequality to get: 
$$| (f(x) -L) +  (g(x) - M) | \leq | f(x) - L | + | g(x) - M| $$
Now because we want the whole expression to be $< \epsilon$, we can make each term less than half of $\epsilon$ 
$$| (f(x) -L) | < \frac{\epsilon}{2}$$
$$| (g(x) -M) | < \frac{\epsilon}{2}$$
After adding the expressions above we have shown that 
$$| f(x) - L | + | g(x) - M| < \epsilon$$
Similar method can be used to prove the other properties in the arithmetic of limits 
### Evaluating polynomials 

Let $p(x)$ and $q(x)$ be polynomials and $a \in \mathbb{R}$  s.t. $q(a) \neq 0$. Then 

$$\lim_{x \to a} \frac{p(x)}{q(x)} = \frac{p(a)}{q(a)}
$$
The proof is built from the limit properties in the section before. So we don't need to do any $\epsilon-\delta$ proofs as we can assume the laws of arithmetic for limits 

### Squeeze theorem + proof 

Imagine we have three functions: 

$$f(x) \leq g(x) \leq h(x), \space \forall x \text{ near a except maybe at a itself}$$

If both the outer functions $f$ and $h$ "squeeze" towards the same limit $L$ as $x \to a$, then the middle function $g$ will also tend towards $a$. 

We can use the inequality property to prove this theorem. 

### One-sided limits  

Sometimes, we only care about how a function behaves as $x$ approaches a point from either the left or the right. 

Let $f$ be a function defined on an interval around $a$ 

The right hand limit (approaching from values greater than $a$) is defined as: 

$$\lim_{x \to a^+} f(x) = L \iff \forall \epsilon > 0, \exists \delta > 0, \space s.t. \space 0 < x-a < \delta \implies | f(x) - L | < \epsilon $$

And the left hand limit (approaching from values smaller than $a$) is defined as: 
$$\lim_{x \to a^-} f(x) = L \iff \forall \epsilon > 0, \exists \delta > 0, \space s.t. \space 0 < a-x < \delta \implies | f(x) - L | < \epsilon  $$
If $\lim_{x \to a^+} f(x) \neq \lim_{x \to a^-} f(x)$ , then the limit does not exist

Notice how in the one sided limit, there are no absolute value signs. This is because from the right hand side, the distance is already positive. If we did write $0 < |x-a| <$ for one sided limits, then it would allow $x$ to approach from both directions, which is not what we want. 
### Limits at Infinity 

Now, instead of approaching a finite point $a$, we can consider what happens as $x$ grows without bound or decreases without bound 

$$\lim_{x \to \infty} f(x) = L \iff \forall \epsilon > 0, \exists N > 0, \space s.t. x > N \implies | f(x) - L | < \epsilon $$

Similarly, 
$$\lim_{x \to -\infty} f(x) = L \iff \forall \epsilon > 0, \exists N > 0, \space s.t. x <- N \implies | f(x) - L | < \epsilon$$

For a limit to exist, $\lim_{x \to a} f(x) = L$ means that the value of $f(x)$ gets arbitrarily close to a finite number $L$, so if no such finite $L$ exists, then the limit does not exist. 
So the statement $\lim_{x \to \infty} f(x) = \infty$ just means that $f(x)$ grows without a bound as $x$ grows without a bound. 

# 3. Continuity 

## Continuous Functions

Intuitively, continuous functions are those that we can draw without lifting the pencil off the page. 
[[Tags/Definition\|Definition]] A function $f$ is **continuous** at a point $a$ if $$ \lim_{x \to a} f(x) = f(a)$$
A function that is non-continuous is called **discontinuous**

Think back to limits, limits don’t care about what happens at a point, but continuity does. 

Now we want to think about what it means for a function to be continuous on an interval. Just how we can take limits from the left and right, we can do the same for continuity: 

[[Tags/Definition\|Definition]] A function $f$ is continuous at $a$ on the right if 
$$ \lim_{x \to a^+} f(x) = f(a) $$
And it’s continuous on the left if $$ \lim_{x \to a^-} f(x) = f(a) $$
### Continuity in an interval 

[[Tags/Definition\|Definition]] A function $f$ is continuous (conts) on $(b,c)$ if it is conts at $a$ $\forall a \in (b,c)$

If we were to restrict it to a half-open interval, then we would have to do one-sided continuity as we could only come in from the left or the right 

[[Tags/Definition\|Definition]] A function $f$ is conts on $[b,c]$ if it is conts at $a$ $\forall a \in (b,c)$ and it is conts on the right at $x=b$ and and conts on the left for $x=c$ 

### Arithmetic for Continuous functions
The arithmetic of limits is the same as arithmetic for continuous functions, and they are listed here below. Continuity boils down to limits, everything in calculus boils down to limits. 

Suppose $f$ and $g$ are conts at $x=a$, then 
- $f+g$ is conts at a 
- $f-g$ is conts at a 
- $fg$ is conts at a 
- $\frac{f}{g}$ is conts at a, provided $g(a) \neq 0$ 
- $cf$ is conts at $a$ for any constant $c$ 

We can prove one of these properties below: 

As $f$, $g$ are conts at $a$, then $\lim_{x \to a} f(x) = a$ and $\lim_{x \to a} g(x) = a$ 

So by the arithmetic of limits and defn on continuity we have: 
$$ \lim_{x \to a} (f+g)(x) = \lim_{x \to a} (f(x) + g(x)) = f(a) + g(a) = (f+g)(a) $$
As we did for limits, we can also have continuity for polynomials and composite functions: 

We have that any polynomial $p(x)$ is continuous at $a \space \forall a \in \mathbb{R}$, and any function $\frac{p(x)}{q(x)}$ Is continuous at $a$ provided that $q(a) \neq 0$ 

Now for the **composition**: if $g$ is conts at $a$, and if $f$ is conts at $g(a)$, then $f \circ g$ is conts at $a$ 

For the proof for the above, we want to think about the defn of composition, so 
$$ (f \circ g) (a) = f(g(a))$$
So we want $g$ to be conts at $a$, and then if $f$ is conts at $g(a)$, we have that the composition is conts at $a$. The actual proof of said to be more confusing than enlightening 

### Intermediate Value Theorem (IVT) 

The intuitive idea behind this is, when we have two points connected by a continuous curve with one point below the line and another point above the line, then there is at least one place where the curve crosses the line. 

[[Tags/Definition\|Definition]] More formally, if a function $f$ is a continuous function on the interval $[a,b]$ and $K$ is a number such that $f(a) < K < f(b)$, then $\exists c \in (a,b)$ such that $f(c) = K$. 

IVT is useful for a number of reasons, one of the applications is to find zeroes of a function, especially when we cannot do so by factoring 

Consider the example below: 
Show that $\sin x + 2 \cos x - x^2 = 0$ has a solution 

At the moment this is an equation, so let’s turn into into a function 
Let $f(x) = \sin x + 2 \cos x - x^2$, and now we want to show that $f(c) = 0$ for some $c$ 

We know that $f$ is conts because it is the sum of different conts functions by the arithmetic of conts functions. 

And now we want to pick two points

$$ f(0) = 2 > 0 $$ $$ f(\pi /2) = 1 -(\pi/2)^2 < 0 $$
So by the IVT, there is a $c \in (0, \pi/2) s.t. f(c) = 0$

#### Proof of the IVT (not something we’ll be tested on) #explainbetter 

The IVT essentially says that if $f: [a,b] \in \mathbb{R}$ is conts, and $K$ is such that $f(a) < K <f(b)$, then there exists at least one $c \in (a,b)$ such that $f(c) = K$ 

And now, we want to prove that such a $c$ exists. So our idea is to to search for where $f$ crosses the level $K$ (and this is where bounds will come in), and then use the continuity of $f$ to guarantee that we can trap that crossing point 

We want to show that $\exists c \in [a,b]$ with $g(c) = 0$ 

First step is to define a set, so let 
$$ S = \{  x \in [a,b] \space g(x) \leq 0 \}$$
This means $S$ collects all points where $f(x) \leq K$ 

Some goofy algebra proof 

 
### Extreme Value Theorem 

#### Maximum and Minimum 

Before we talk about maximum and minimum, we need to define the terms lower and upper bounds 

[[Tags/Definition\|Definition]] A fn $f$ on an interval $I$ has an **upper bound** $M$ if $f(x) \leq M \space \forall x \in I$ 

[[Tags/Definition\|Definition]] $f$ has a **lower bound** $N$ if $f(x) \geq N \space \forall x \in I$

[[Tags/Definition\|Definition]] Let $f$ be a fn on an interval $I$. Then $f$ has a **maximum** $M$ if $M$ is an upper bound and there is a $c \in I \space s.t. f(c) = M$

$f$ has a **minimum** $N$ if $N$ is a lower bound and there is a $d \in I \space s.t. f(d) = N$

And now we can construct the definition for the extreme value theorem: 

[[Tags/Definition\|Definition]] 
Suppose that $f(x)$ is a continuous on the interval $[a,b]$, then there are two numbers $a \leq c, d \leq b$ such that $f(c)$ is an **absolute maximum** for the function and $f(d)$ is the an **absolute minimum** for the function.  

So if we have a continuous function on an interval , then we are guaranteed to have both an absolute maximum and an absolute minimum somewhere in the interval. The theorem doesn't tell us where they will occur or if they occur more than once, but we do know that they do exist somewhere. 

---

# 4. Differentiation 

At its core, differentiation is measures how fast something is changing, the rate of change. If $f(x)$ is a curve, then its derivative at a point $a$ is just the slope of the tangent line to the curve at that point. 

To generalise this into a definition, take two points on a function $f(x)$
- $(x, f(x))$ 
and a point slighter further up the curve: 
- $(x+h, f(x+h))$

The the average rate of change (i.e. slope of the **secant line**) is given: 
$$ \frac{f(x+h) - f(x)}{x+h -x}$$
Now if we let $h \rightarrow 0$, then the secant line becomes a tangent, and the limit gives us the formal definition of the derivative: 
$$ f^`(x) = \lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h} $$
#### Example with note of $\sqrt{x}$

Not all functions are differentiable in their domain. Consider the function 

$$ f(x) = \sqrt{ x }$$
The domain of the function is $[0, \infty)$

But the derivative is not defined at at $0$ as derivatives are based on limits, and the left-hand limit $h \rightarrow 0^-$ does not exist 

## Differentiability vs Continuity 

A differentiable function is continuous. But a continuous function doesn’t have to be continuous 

We just need a counterexample to prove the second statement above false. Consider the following function which is continuous: 
$$ f(x) = |x| $$
$$(0, \infty), f(x) = x$$
$$ (-\infty, 0), f(x) = -x $$
We can observe the following because of the gradient of tangent line (derivative):
$$ \lim_{  h \to 0^+ } \frac{f(x+h)-f(x)}{h}  = 1$$
$$ \lim_{ h \to 0^-} \frac{f(x+h)-f(x)}{h} = -1 $$

The limits from the left and right are not equal, so the limit does not exist, so the function is not differentiable at $0$. Geometrically, at $x=0$, the gradient changes abruptly from $-1$ to $1$ 

Therefore, $f(x) = |x|$ is conts. on $\mathbb{R}$ and differentiable on $(-\infty, 0) \cup (0, \infty)$

### Proof: differentiability $\implies$ continuity  

As $f$ is differentiable, we can use the definition to say that: 

$$ f^`(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h} \text{ exists }$$
Now if $f$ is differentiable at some point $x=a$, then: 

$$ f^`(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h} $$
And based on the defn. of continuity, we want to show that $$ \lim_{ x \to a} f(x) = f(a) $$ 
So let $h = x-a \implies x = a+h$ 
By the arithmetic of limits we have: 
$$ \lim_{ x \to a } f(x)  - f(a) = \lim_{ h \to 0 }[f(a+h) - f(a)] $$

We have multiply and divide by $h$ to get: 

$$ f(a+h) - f(a) = h \cdot \frac{f(a+h) -f(a)}{h} $$
And now when we take limits: 
$$ \lim_{ h \to 0 }[f(a+h) - f(a)] = \lim_{ h \to 0 } h \cdot \frac{f(a+h) - f(a)}{h} $$
Since we know that the derivative exists, we have by the arithmetic of limits: 
$$ \lim_{ h \to 0 }\frac{f(a+h) - f(a)}{h}  = f^`(a) \text{ and } \lim_{ h \to 0 } = 0 $$
Therefore, 
$$ \lim_{ h \to 0 }[f(a+h) - f(a)] = 0 $$
So as $$  \lim_{ x \to a } f(x)  - f(a)  = 0 \implies \lim_{x \to a} f(x) = f(a_{}) $$

## Arithmetic of Differentiable functions

As with functions and limits and continuity, there is arithmetic of differentiable functions: 

$$ (f+g)^` (x) = f^`(x) + g^`(x)$$
$$ (f-g)^` (x) = f^`(x) - g^`(x)$$
Next up is the **Product Rule**
$$ (f\cdot g)^` (x) = f^`(x) \cdot g(x) + f(x) \cdot g^`(x)$$
And the **Quotient rule**

$$(\frac{f}{g})^`(x) = \frac{f^`(x)g(x) - f(x)g^`(x)}{(g(x))^2} $$
### Proof of the Product rule 

To be done by future me, so I’ll just add a useful link **[here](https://tutorial.math.lamar.edu/classes/calci/DerivativeProofs.aspx)** 

One we have this, we can use the product rule to prove the quotient rule by writing the quotient as $(f \cdot g^{-1} )^`(x)$

### Power rule 

$$f(x) = x^n, \implies f^`(x) = nx^{n-1}, \space \forall n \geq 1$$

This can be proved by induction and the product rule 
Base case is $n=1$, so $f^`(x) = 1 = 1 \cdot x^0$ 

Now assume that the rule holds for some $n=k$ 
So $f^`(x^k) = kx^{k-1}$

Observe that $$ x^k = x^k \cdot x$$
So we can apply the product rule to get: 

$$ f^`(x^{k+1}) = (x^k)^` \cdot x + x^k \cdot (x)^`$$
From our inductive case we know that: 
$$ (x^k)^` = kx^{k-1}$$
and that $(x)^` = 1$ 

So 
$$ f^`(x^{k+1}) = (kx^{k-1}) x + x^k (1) = (k+1)x^k$$
So our assumptions works for $n= k+1$

If true for $n=k$, it's also true for $n=k+1$. As our assumption is true for $n=1$, by mathematical induction it's holds $\forall n \in \mathbb{Z}^+$

### Differentiating polynomials 

If 

$$ p(x)= a_n x^n + a_{n-1}x^{n-1} + … + a_1x + a_0 $$
Then 
$$p^`(x) =  a_{n}nx^{n-1} + a_{n-1}(n-1)x^{n-2} … + a_1$$
## Derivative as a Rate of Change 

There is more than one way to think of what a derivative is for a function $f(x)$. 
It can either be viewed as the gradient of the tangent line to the curve $f(x)$ as $x$. 

Or, as a rate of change, i.e. the change in $f$ values in proportion to the change in $x$ values, namely 
$$ \frac{f(x+h)-f(x)}{h} $$

If we take limits, then we get the instantaneous rate of change: 

$$ \lim_{h \to 0} \frac{f(x+h)-f(x)}{h} = f^`(x)$$

In this course, we will be using **Leibniz** notation for the derivative: comes from the rate of change 

Given a fn $y = f(x)$, then 

$$ \frac{dy}{dx} = f^`(x) $$
Which basically is the rate of change of $y$ values in proportion to change of $x$ values 

### Chain rule 

Essentially a method for taking the derivative of a composite function 

Let $y = f \circ g$ Then $y = f(u)$ where $u = g(x)$

So the rate of change of $y$ with respect to $x$ depends on the rate of change of $y$ with respect to $u$ and rate of change of $u$ with respect to $x$. 
$$ \frac{dy}{dx}  = \frac{dy}{du} \frac{du}{dx}$$
Going back to our definition for composite function. 

We have $y = f \circ g$, so $y = f(g(x))$ 

$$ (f \circ g)^`(x) = f^`(g(x))g^`(x) $$
## Trig functions - key properties 

$$ \frac{d}{dx} (\sin x) = \cos x$$
$$ \frac{d}{dx} (\cos x) = -\sin x$$
$$ \frac{d}{dx} (\tan x) = \sec^2 x$$
$$ \frac{d}{dx} (\sec x) = \sec x \tan x$$
$$ \frac{d}{dx} (\csc x) = -\csc x \cot x$$
$$ \frac{d}{dx} (\cot x) = -\csc^2 x$$
### Proof of $(\sin x)^` = \cos x$ (mostly left to the reader)

We need to assume two lemmas here: 

$$ \lim_{x \to 0} \frac{\sin x}{x} = 1  $$
$$ \lim_{x \to 0} \frac{\cos x-1}{x} = 0  $$
Using these definitions and the compound angle formula for $\sin(x)$, the proof is left as an exercise to the reader  
$$ (\sin x)^` = \lim_{h \to 0} \frac{\sin(x+h)-\sin x}{h}  = \cos (x)$$

## Exponentials and Logarithmic Functions 

Just copy from the notes here for the first principles 

$$ (a^x)^` = a^x \cdot f^`(0) $$
Where $f^`(0)$ is a constant. There is a unique $a$ with $f^`(0) = 1$ This is when $a=e$ 


Lemma: $$ (\ln x)^` = \frac{1}{x} $$
As $\ln x$ and $e^x$ are inverse functions: 
$$e^{\ln x} =x $$
And now we can differentiate using the chain rule 
$$ e^{\ln x} \cdot \frac{d}{dx}(\ln x) = 1 $$
$$ x \cdot \frac{d}{dx}(\ln x) = 1$$
$$\implies \frac{d}{dx} = \frac{1}{x} $$
$$ \square$$
So $$ (a^x)^` = a^x \cdot \ln a $$
$$ (log_ax)^` = \frac{1}{x \ln a}$$
## Hyperbolic Trig Functions 

$$ \sinh (x) = \frac{e^x - e^{-x}}{2}$$
Some properties of $\sinh (x$): 
- Odd function 
- Domain = $\mathbb{R}$ 
- Range = $\mathbb{R}$ 
$$ \cosh (x) = \frac{e^x + e^{-x}}{2}$$
Some properties of $\cosh (x)$ 
- Even function 
- Domain = $\mathbb{R}$ 
- Range = $[1, \infty)$

Notice how the trig function $\cos^2x + sin^2x = 1$ means they like on the circle $x^2 + y^2 = 1$. Similarly, 
$$ \cosh^2x - \sinh^2x = 1 $$
Means the hyperbolic trig functions like on the hyperbole $x^2 - y^2 = 1$ 

Some other key derivatives, they can proved by writing the hyperbolic in the terms of exponentials

$$ (\sinh x)^` = \cosh x $$
$$ (\cosh x)^` = \sinh x$$
$$ \tanh x = \frac{\sinh x}{\cosh x}$$

## Implicit Differentiation 

When we have functions that are in terms of both $x$ and $y$, eg: 
$$ y^3 - x^2 = 3$$
We can’t solve explicitly for $y$ as the function is defined implicitly. So to differentiate, we need to use the chain rule: 
$$ 3y^2 \cdot y^` - 2x = 0 $$
$$ y^` = \frac{2x}{3y^2} $$
One of the things we can do with implicit is proof that derivative of rational powers 

$$ (x^\frac{p}{q})^` = \frac{p}{q}(x^{\frac{p}{q}-1})^`$$

## Inverse Trig Functions 

We need to restrict the functions so that they are a bijection and so we can find their inverse 

$$ \sin x : [\frac{-\pi}{2}, \frac{\pi}{2}] \rightarrow [-1,1] $$
$$ \sin^{-1} x : [-1,1] \rightarrow [\frac{-\pi}{2}, \frac{\pi}{2}]$$

Then $(\sin ^{-1} x)^`$ is 

Let $y = sin^{-1} x \implies \sin y = x$

And then we can differentiate implicitly: 

$$ \cos y \cdot y^` = 1$$
$$ \implies y^` = \frac{1}{\cos y}$$
We know by the trig identity that $\cos^2y + \sin^2y = 1 \implies \cos y = \sqrt{1 - \sin
{ #2}
 y}$

Hence, after substituting, we get the inverse of the trig functions: 
$$ (\sin^{-1}x)^` = \frac{1}{\sqrt{1-x^2}} $$
$$ (\cos^{-1}x)^` = -\frac{1}{\sqrt{1-x^2}} $$
$$ (\tan^{-1} x)^` = \frac{1}{1+x^2}$$
For the inverse of $\tan x$, we uses the identity that $1 + \tan^2 x = \sec^2x$
# 5. Curve Sketching

Let $f$ be a differentiable function, then a point $c$ is called a **critical point** if $f^`(c) = 0$

[[Tags/Definition\|Definition]] $f$ has a **local minimum** in an interval $I$ if $f(x)_0 \leq f(x) \space \forall x \in I$

[[Tags/Definition\|Definition]] $f$ has a **local maximum** in an interval $I$ if $f(x)_1 \geq f(x) \space \forall x \in I$

## Maximum and Minimums 
### Proof of local minimum and maximum 
So if $f$ is differentiable on $(a,b)$ and has a local max/local min on point $c$, then $f^`(c) = 0$ 

We can prove the above by considering the limit definition at the point $c$ 

Suppose that $c$ is a local max on $(a,b)$ 

This means by definition, there exists some small interval around $c$ such that: 
$$ f(x) \leq f(c) \space \forall x \text{ near a}$$
Now if we pick an $h$ value that is positive and lands in the interval 

Let $h > 0$ s.t. $c+h \in (a,b)$ so that the value is still defined 

Now $c$ is a local maximum, so 

$$f(c) \geq f(c+h) \implies f(c+h) - f(c) \leq 0 $$
After dividing both sides by $h$ we have: 
$$ \frac{f(c+h) - f(c)}{h} \leq 0$$
And now we can take the limit 
 $$\implies  \lim_{h \to 0^+} \frac{f(c+h) - f(c) }{h} \leq 0 $$
As $f$ is differentiable, the limit from left equals limit from right, so this equals $f^`(c)$ 

Now we let $h < 0$ s.t. $f(c+h) - f(c) \geq 0$
$$\implies  \lim_{h \to 0^-} \frac{f(c+h) - f(c) }{h} \geq 0 $$
Once again, as $f$ is differentiable, so the left and right hand limits match, so this also equals $f^`(c)$ 

Now we have that $0 \leq f^`(c) \leq 0$ , hence $f^`(c) = 0$ 

### Global minimum and maximum 

[[Tags/Definition\|Definition]] A fn $f$ has an **absolute (global) maximum** at $x_0$ if $f(x_0) \geq f(x) \space \forall x \in F$ 
[[Tags/Definition\|Definition]] A fn $f$ has an **absolute (global) minimum** at $x_1$ if $f(x_1) \leq f(x) \space \forall x \in F$ 


There are also different kinds of local/global minimums and maximums 


[[Tags/Definition\|Definition]] A point $c$ where $f$ is conts but not differentiable is called a **singular point**

Extreme values (local max, local min) occur at: 
- End points - derivative isn’t even defined at these points at times
- Critical points 
- Singular points 

## Mean Value Theorem (MVT) 

This will help us identify where the graph of $f$ increase or decreases 

[[Tags/Definition\|Definition]] 
Let $f$ be a **conts** fn on $[a,b]$ that is **differentiable** on $(a,b)$. Then there is a point $c \in (a,b)$ s.t. 

$$ f^`(c) = \frac{f(b) - f(a)}{b-a} $$

Think of it as the gradient of a secant line of joining two points on a graph. So what this is saying is that there is some point $c \in (a,b)$  such the gradient of a tangent line equals the secant line are the same 
### Proof of the MVT 

The formal proof involve Rolle's Theorem. The idea here is that we want to "remove" the secant line so the endpoints are level. 

Let $g(x) = f(x)$ - equation of secant line. 

The secant line passing through $(a, f(a))$ and $(b, f(b))$ has the gradient: 
$$m = \frac{f(b) - f(a)}{b-a} $$
And now we can use the straight line equation to get: 
$$ y - y_{1} =  m(x - x_{1})$$
$$\implies y- f(a) = \frac{f(b) - f(a)}{b-a} (x-a)$$
Rearranging for $y = L(x)$, we get: 
$$ L(x) = f(a) + \frac{f(b) - f(a)}{b-a} (x-a)$$ So we define 
$$ g(x) = f(x) - L(x)$$
Now, we check $g$ at the endpoints 
$$ g(a) = f(a) - L(a) = f(a) - f(a) = 0$$
$$ g(b) = f(b) - L(b) = f(b) - \left[ f(a) + \frac{f(b) - f(a)}{b-a}(b-a) \right] = 0 $$
So we have that $g(a) = g(b) = 0$ 

Using Rolle's Theorem (which is a special case of the MVT), we have that if a fn is conts on $[a,b]$ and differentiable on $(a,b)$ and $g(a) = g(b)$, then $\exists c \in (a,b)$ s.t. $g^`(c) = 0$. 

What we want is to apply that special case, to the general case, and we have done that by removing the secant line equation. 

And as our function $g$ satisfies, so $g^`(c) = 0$ 

Now, we if different $g(x)$, we have: 
$$ g^`(x) = f^`(x) - \frac{f(b) - f(a)}{b-a}$$
And setting $g^`(c) = 0$ gives us the MVT: 
$$ f^`(c) = \frac{f(b) - f(a)}{b-a} $$

Intuitively, the MVT links average change to instantaneous change. 
This will be useful in deriving the Fundamental Theorem of Calculus later in the course

## Intervals of Increasing and Decreasing 

[[Tags/Definition\|Definition]] Let $f$ be a fn on an interval $I$, then ;

- $f$ is **increasing** on $I$ if $\forall x_1,x_2 \in I  \quad x_1 < x_2 \implies f(x_1) < f(x_2)$ 
- $f$ is **decreasing** on $I$ if $\forall x_1,x_2 \in I \quad x_1 < x_2 \implies f(x_1) > f(x_2)$ 

Let $f$ be a fn on an open interval $I$, then: 

$$ f^`(x) > 0 \space \forall x \in I \implies \text{ $f$ is increasing}$$
$$ f^`(x) < 0 \space \forall x \in I \implies \text{ $f$ is decreasing}$$

The proof above uses the MVT: 

First, to use the MVT, we assume that $f$ is conts on $[a,b]$ and differentiable on the $(a,b)$. Then, we pick any two points in that interval: $x_1, x_2 \in [a,b], \quad x_1 < x_2$ 

By the MVT, $\exists c \in (x_1, x_2)$ s.t. 
$$f^`(c) =  \frac{f(x_{2}) - f(x_{1})}{x_{2} - x_{1}} $$
Now we consider cases

Case 1  - $f^`(x) > 0$ everywhere on $(a,b)$ 

Then, $\forall c, f^`(c) > 0$ 
So by the MVT: 
$$\frac{f(x_{2}) - f(x_{1})}{x_{2} - x_{1}} = f^`(c) > 0$$
But as $x_2 - x_1 > 0$, we must have that $f(x_2) - f(x_1) > 0 \implies f(x_{2}) > f(x_{1})$ on $(a,b)$. Therefore by definition, $f$ is strictly increasing 

Case 2-  $f^`(x) < 0$ everywhere on $(a,b)$ 

By the same logic, 

$$\forall c, f^`(c) < 0 \implies\frac{f(x_{2}) - f(x_{1})}{x_{2} - x_{1}} < 0$$
But as $x_2 - x_1 > 0$, we must have that $f(x_2) - f(x_1) < 0 \implies f(x_{2}) < f(x_{1})$ on $(a,b)$. Therefore by definition,  is strictly decreasing

Naturally, if $f^`(x) = 0$ then 
$$  \frac{f(x_{2}) - f(x_{1})}{x_{2} - x_{1}}  = f^`(c) = 0 \implies f(x_{2}) - f(x_{1}) = 0 \implies f(x_{1}) = f(x_{2})$$
So $f$ would be constant in that interval 

## Concavity and Points of Inflection 

[[Tags/Definition\|Definition]] 
Let $f$ be a fn that has a second derivative on an open interval. Then 

-  $f^`$ is increasing on $I$ $\implies$ $f$ is **concave up** on $R$ 
- $f^`$ is decreasing on $I$ $\implies$ $f$ is **concave down** on $R$ 

Graphically, the tangent lines are: 
- Above the graph for a concave down 
- Below the lines for a concave up 

[[Tags/Definition\|Definition]] 
A fn $f$ that has a second derivative has an **inflection point** at $x$ if the **concavity** changes at $x$ and $f^{``}(x) = 0$. 

So if $f$ is a fn whose second derivative exists on an open interval $I$, then 
- $f^{``}(x) > 0$ on $I \iff$ $f$ is concave up 
- $f^{``}(x) < 0$ on $I \iff$ $f$ is concave down
- $f$ has an inflection point at $x \implies$ $f^{``}(x) = 0$ 

## Second Derivative Test 

We can the $f^{``}$ to determine the local max and min 

So let $f$ be a twice differentiable function on some open interval $I$, and for some $c$ ,$f^{``}(c)$ exists, then: 
$$ f^{``}(c) > 0 \implies \text{ $c$ is a local minimum} $$
$$ f^{``}(c) < 0 \implies \text{ $c$ is a local maximum} $$
$$ f^{``}(c) = 0 \implies \text{ more information needed} $$
## Horizontal and Vertical Asymptotes 

[[Tags/Definition\|Definition]] A graph has a **vertical asymptote** at $x=a$ if: 
$$ \lim_{x\to a^+} f(x) = \pm \infty \quad \text{ or } \lim_{x \to a^-}f(x) = \pm \infty $$
[[Tags/Definition\|Definition]] A graph has a **horizontal asymptote** if
$$ \lim_{x \to \infty} f(x) = L \quad\text{ or } \lim_{x \to \infty^-}f(x) = L $$
Where $L$ is some finite number 

The best way to practice this topic- do curve sketching 

# 6. Integration 

## Anti-Derivatives 
 
[[Tags/Definition\|Definition]] Let $f$ be a function, then a function $g$ is the **antiderivative** of $f$ if $g$ is differentiable and $g^` = f$

Now suppose that $g^`(x) = f(x)$. Then $h(x) =g(x) + c \implies h^`(x) = f(x)$  where $c$ is a constant. The proof of this is fairly trivial. But what this means is that antiderivatives are not unique, as for any antiderivative, we can always add a constant to get another anti-derivative 

Geometrically speaking, antiderivative has no meaning, but it will be used in finding integrals. 

## Definite Integral 

Let $f$ be a continuous, and suppose we want to find the area $A$ between the curve and the $x$ axis that lies over $[a,b]$ 

One way to approach this problem is to consider approximating the area of rectangles that we can fit below the curve with total area $L$, and a sequence of rectangles above the curve with a total area $U$. Then we have the area bounded as $L \leq A \leq U$. As the curve isn't made up on neat rectangles, we can approximate the area by taking a limit as those rectangles get thinner and thinner. 

First, we divide our interval, $[a,b]$ into segments: 
$$ [a,x_{1}], [x_{1}, x_{2}], \dots , [x_{n-2}, x_{n-1}], [x_{n-1}, x_{b}], \quad a < x_{1} < x_{2} < \dots < x_{n-1} < b$$
We can let $l_i$ be the length of segment $[x_{i-1}, x_i]$. This division is called a partition, and we label it as $P$. 

Consider restricting $f$ to $[x_{i-1}, x_i]$. So on that closed interval $f$ is continuous so it has a maximum and minimum value by the EVT. Let $M_i$ be that max value, and $m_i$ the min value. 

Now we form rectangles in our restricted interval $[x_{i-1}, x_i]$. The lower rectangle has area $l_im_i$ and the upper rectangle has area $l_iM_i$ 

When we sum the rectangles, the areas of the upper and lower is given as follows: 
$$ L(f,P) = l_{1}m_{1} + \dots + l_{n}m_{n}$$
$$ U(f,P) = l_{1}M_{1} + \dots + l_{n}M_{n} $$
Therefore, we know that our area $A$ is bounded by 
$$ L(f,P) \leq A \leq U(f,P) $$
Now, if we keep increasing $n$, i.e. make the rectangles thinner, then the lower and upper estimates get closer together, because $f$ can't change much over the tiny intervals. It's a bit like the squeeze theorem. 

[[Tags/Definition\|Definition]] Let $f$ be a continuous function on the interval $[a,b]$, then the **definite integral of $f$ from $a$ to $b$** is the unique number $I$ s.t. $L(f,P) \leq I \leq U(,P)$ for all partitions of $[a,b]$. This is written as: 
$$ I = \int_{a}^b f(x) dx$$
### Properties of definite integrals 

There are some nice properties of integrals because of the arithmetic of limits, and how everything boils down to limits 
$$ \int_{a}^b (cf(x) + dg(x)) \,  dx = c\int_{a}^{b}f(x) \, dx +d \int_{a}^{b} g(x) \, dx $$
$$ \int_{a}
{ #a}
 f(x) \ dx = 0$$
$$ \int_{a}^{t} f(x) \ dx + \int_{t}^{b}f(x) \ dx = \int_{a}^{b} f(x) \ dx  $$
$$ \int_{b}^{a} f(x) \ dx = - \int_{a}^{b} f(x) \ dx  $$
$$ f(x) \leq g(x)  \quad \forall x \in [a,b] \implies \int_{a}^{b} f(x) \ dx \leq \int_{a}^b g(x) \ dx $$

## Fundamental Theorem of Calculus 

There is a reason this is called the Fundamental Theorem of Calculus. Not only it shows us the relationship between integration and differentiation, but it also guarantees that any integrable function has an antiderivative, it guarantees that any continuous function has an antiderivative 
### Part I

If $f$ is a continuous function over an interval $[a,b]$, and the function $F(x)$ is defined by: 
$$ F(X) = \int_{a}^x f(t) \ dt$$
Then $F^`(X) = f(x)$ over $[a,b]$ 

So $F(X)$ is the area under $f$ from $a$ to $x$, it's the area accumulation function. 

To show this holds, we apply the definition of the derivative to our function to get:: 

$$F^`(x)  =\lim_{ h \to 0 } \frac{F(x+h) - F(x)}{h} $$
$$  = \lim_{ h \to 0 } \frac{1}{h} \left[ \int_{a}^{x+h} f(t) \ dt - \int_{a}^{x} f(t) \ dt \right] $$
After splitting the integral we have: 
$$ = \lim_{ h \to 0 } \frac{1}{h} \left[ \int_{a}^{x} f(t) \ dt + \int_{x}^{x+h} f(t) \ dt -\int_{a}^{x} f(t) \ dt \right]$$
$$ = \lim_{ h \to 0} \frac{1}{h} \int_{x}^{x+h} f(t) \ dt   $$
Now we either estimate this using a lower and upper bound (which is how it's given in the notes), or we can use the Mean value theorem. 

Notice that $\frac{1}{h} \int_{x}^{x+h} f(t) \ dt$ is just the average value of the function $f(x)$ over the interval $[x, x+h]$. So by the MVT, $\exists c \in [x,x+h] s.t.$: 
$$  \frac{1}{h} \int_{x}^{x+h} f(t) \ dt  = f(c)$$
And now we can take limits, since $c$ is between $x$ and $h$, and $c \to x$ and as $h \to 0$ and $f$ is continuous 
$$ \lim_{ h \to 0 } f(c) = \lim_{ c \to x }  = f(x)$$
So combining all of this together we have: 
$$ F^`(x) =  \frac{1}{h} \int_{x}^{x+h} f(t) \ dt = \lim_{ h \to 0 }f(c) = f(x) $$
$$\square$$

### Part II 

If $f$ is continuous over the interval $[a,b]$, and $F(X)$ is any antiderivative of $f(x)$, then 
$$ \int _{a}^b  f(x) \ dx = F(b) - F(a)$$
What this means is that if we can find an antiderivative for the integrand, then we can evaluate the definite integral by evaluating the antiderivative at the **endpoints** of the interval 

The proof can be done two ways again: using Riemann sums and using the definition of an antiderivative, both make use of the MVT. This one is similar to the one given in notes, but I attempted to explain it more detail: 

Suppose $F$ is an antiderivative of $f$, with $f$ being continuous of $[a,b]$. Now let: 
$$ F(x) =  \int_{a}^{x} f(t) \ dt, \quad G(x) = \int_{a}^{x} f(t) \ dt$$
By Part I, we know that $G$ is also an antiderivative of $f$ 
So we have that $F(x) = G(x)$. 

Now, if two functions have the same derivative, then their difference has derivative $0$: $F^` - G^` = 0$ 

So by the MVT, this implies that $F - G$ is a constant function, i.e .$\exists c \in [a,b]$ s.t. $G(x) = F(x) + c$. When we let $x=a$ and compute $G(a)$ we have: 
$$ F(a) + c = G(a) = \int _{a}^a f(t) \ dt = 0 \implies c = -F(A)$$
So we have that $G(x) = F(x) - F(a)$.

And then we evaluate at $x=b$ we have $G(b)$ and using the definition of $G(x)$ above we have: 
$$ \int_{a}^b f(x) \ dx = G(b) = F(b) - f(a) \quad \square $$








































