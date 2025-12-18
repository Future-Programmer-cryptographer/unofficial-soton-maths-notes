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

$$ a^0 = 1 $$
$$ a^{-x} = \frac{1}{a^x}$$
$$a^x a^y = a^{x+y} \ \ \forall x,y \in \mathbb{R} $$
$$(a^x)^y = a^{xy} \  \ \forall x,y \in \mathbb{R} $$
$$(ab)^x = a^{x}b^x \  \ \forall a,b \in (0, \infty) $$

$a^x$ is also a bijection so it has an inverse function 

[[Tags/Definition\|Definition]] The **logarithm** with base a is the function: 
$$ \log_a  : (0,\infty) \rightarrow \mathbb{R}$$
Defined by $log_a(x) = y$ iff $a^y = x$

$$ log_a(a^x) = x $$
$$ a^{log_ax} = x  $$


Properties: 
$$ \log_{a} (1) = 0$$
$$ \log_{a}({\frac{1}{x}})  =  - \log_{a} (x)$$
$$ \log_{a} (xy) =  \log_{a}x + \log_{a} y $$
$$ \log_{a} (x^y) =  y \log_{a}(x) $$
$$ \log_{a} (x) =  \frac{\log_{b}(x)}{\log_{b}(a)} $$

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

#### Proof of the IVT (not something we’ll be tested on) 

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
## Area Problem 

Suppose $f(x) \geq g(x)$ on $[a,b]$ and we want to find the area between $f$ and $g$ 

So the area is given as: 
$$ \int_a^b f(x) - g(x) \ dx $$
If it’s not immediately obvious which curve is above, then we can evaluate the function at a point in the interval $(a,b)$  

# 7. Methods of Integration 

## Substitution 

This is like the integration version of chain rule 

So by the chain rule we have that: 
$$ \frac{d}{dx} f(g(x)) = f^`(g(x))g^`(x)$$
And when we integrate we have: 
$$ \int f^`(g(x))g^`(x) = f(g(x)) + c$$
Now if we let $u = g(x)$ then $\frac{du}{dx} = g^`(x) \implies du = g^`(x)\ dx$ 

After substituting in we have: 
$$ \int f^`(g(x))g^`(x) = \int f^`(u) + c = f(u) + c = f(g(x)) + c$$
It's important to not that the derivative is not a fraction, and the proper proof for why the fraction thing works is covered in Differentials 
 
### Interesting Trig odd and even properties  

Below are the half angle formulas for sine and cosine which will be useful in integrating even powers of trig functions 
$$ \cos^2x = \frac{1}{2}(1+\cos 2x)$$
$$ \sin^2 x = \frac{1}{2}(1- \cos 2x)$$

To generalise: 

$$ \int \sin^m x \cos^n x \ dx $$
If either one of $m$ or $n$ is odd, then we can do this integral by substituting. This is because we will need at least one odd power to cancel out when we're substituting. 

If both $m$ and $n$ are even, then we must use the half angle properties 

## Trig Substitutions 

$$\int \sqrt{a^2 - x^2} \implies x = a \sin \theta $$
$$\int \sqrt{a^2 + x^2} \implies x = a \tan \theta $$
$$\int \sqrt{x^2 - a^2} \implies x = a \sec \theta $$

## Integration by Parts 
$$ \int u  \ dv = uv - \int v \ du $$
## Partial Fractions 

Good for integrals in the for: 
$$ \int \frac{P(x)}{Q(x)} \ dx $$
The reason we can factor $Q(x)$ is because of the Fundamental Theorem of Algebra, which will be covered in Complex Analysis in Year 3 

There are basically 3 main case cases of denominators 

### Case 1: Distinct linear factors 

If $Q(x) = (x-a) (x-b)(x-c)\dots$

Then $$ \frac{P(x)}{Q(x)} = \frac{A}{x-a} + \frac{B}{x-b} + \frac{C}{x-c}$$
To find $A,B,C$, multiply both sides by the denominator and equate coefficients or substitute roots 

### Case 2: Repeated Linear Factors 

If $Q(x) = (x-a)^n$ 
Then all we need is all powers up to $n$: 
$$ \frac{P(x)}{(x-a)^n} = \frac{A_{1}}{x-a} + \frac{A_{2}}{(x-a)^2} + \dots + \frac{A_{n}}{(x-a)^n}$$
### Case 3: Irreducible Quadratic factors 
If the denominator has a quadratic that doesn't factor, then we can can't split it into linear factor like $\frac{A}{x-a}$, so the next thing is to have $\frac{Ax+b}{ax^2 + bx + c}$

This works because $Ax+b$ is the most general linear numerator 

So if $Q(x) = ax^2  + bx+ c$ 

Then $$ \frac{P(x)}{ax^2 + bx+ c} = \frac{Ax +b}{ax^2 + bx+c} $$
# 8. Indeterminate Forms and Improper Integrals 

## L'Hôpital Rule 

This is useful when a limit essentially gives us: 
- $\frac{0}{0}$
- $\frac{\infty}{\infty}$

Because in these cases, the functions go to zero, or infinity at the same time, and we want to know which one goes to zero or infinity faster, so we can compares their rates of change (i.e. derivatives) to find that. There are two versions of this: 

Let $f,g$ be differentiable and $g^`(x) \neq 0$, 
### Version 1 

Suppose $\lim_{x \to a} f(x) = 0$ and $\lim_{x \to a} g(x) = 0$, then 

$$ \lim_{ x \to a } \frac{f^`(x)}{g^`(x)}= L \implies \lim_{ x \to a } \frac{f(x)}{g(x)} = L$$
### Version 2 

Suppose $\lim_{x \to a} f(x) = \pm \infty$ and $\lim_{x \to a} g(x) = \pm \infty$, then 
$$ \lim_{ x \to a } \frac{f^`(x)}{g^`(x)}= L \implies \lim_{ x \to a } \frac{f(x)}{g(x)} = L$$


And note that $a$ here can be $\pm \infty$ 
$e^x$ grows faster than any polynomial, $\ln x$ grows slower than any polynomial, 

#### Fun example

$$ \lim_{x \to 0^+} x^x $$
We we can do some manipulation to get $\ln(x^x) = x \ln x$ and then: 
$$ \lim_{ x \to 0^+ } x \ln x = \lim_{ x \to 0^+ }  \frac{\ln x}{\frac{1}{x}}= \lim_{ x \to 0^+ } \frac{\frac{1}{x}}{-\frac{1}{x^2}} = \lim_{ x \to 0^+ } -x = 0    $$
So to get back to the limit of $x^x$, we need to exponentiate this so we have: 
$$ \lim_{ x \to 0^+ } x^x = e^0 = 1 $$
Pretty cool right! 

### Cauchy’s Mean Value Theorem 

Before proving L’Hôpital, we need to prove the generalised version of the MVT. 

The idea behind this is that if two functions satisfy the conditions of MVT, then some point $c$ exists for where the ratio of their derivatives equals the ratio of their total changes. 

So if $f,g$ are continuous on $[a,b]$ and differentiable on $(a,b)$, and $g^`(x) \neq 0$ then 
$$  \exists c \in (a.b) \ s.t. \ \frac{f^`(c)}{g^`(c)} = \frac{f(b)- f(a)}{g(b) - g(a)}$$

Similar to the proof of Rolle's Theorem and the MVT, we want to generate a function whose endpoints match, apply Rolle's Theorem, and then rearrange to get the expression 

The full proof is in the lecture notes, and very similar to MVT, so I won't write it again here
### Proof of L’Hôpital 

The strategy here is to essentially apply CMVT to $f$ and $g$ on $[a,x]$ 
This gives us $\frac{f(x)}{g(x)} = \frac{f(c)}{g(c)}$
And then since $\exists c \in (a,x)$ when $x \to a$ then $c \to a$ 
We can then take limits one the right hand side and conclude 

## Improper Integrals 

An integral becomes improper if either the interval is infinite or there is a vertical asymptote. 

Eg:

$$ \int_{1}^\infty \frac{1}{x^2} \ dx, \quad \int_{0}^1 \frac{1}{\sqrt{x }} \ dx  $$
In these cases, the Riemann definition using sums of rectangles doesn't work, so we need to work using limits. 

### Integrals converging/diverging  

Consider this example of a function: 
$$ \int _{a}^\infty f(x) \ dx$$
If a limit exists of this integral: 
$$ \lim_{ b \to \infty } \int_{a}^b f(x) \ dx = L $$
Then, the integral **converges** to $L$. If the limit does not exist, then the integral **diverges**

We can use the limit definition to show that $\int_a^{\infty} \frac{1}{x} \ dx$ diverges 
$$  \int_{1}^b \frac{1}{x} \ dx = \ln x |_{1}^b = \ln(b) - \ln(1) = \ln b$$
$$ \lim_{ b \to \infty }  \int_{1}^b \frac{1}{x} \ dx = \lim_{ b \to \infty } \ln b = \infty $$
So since the limit does not exist, the integral diverges 

Similarly, we can use limits again to show that  $\int_a^{\infty} \frac{1}{x^2} \ dx$ converges 
$$ \int_{1}^b \frac{1}{x^2} \ dx = -\frac{1}{x} | _{b}^1 = - \left(  \frac{1}{b} - 1 \right) = 1 - \frac{1}{b} $$
$$ \lim_{ b \to \infty } \int_{1}^b \frac{1}{x^2}  \ dx = \lim_{ b \to \infty } 1 - \frac{1}{b} = 1   $$
So as the limit exists, the integral converges to $1$ 

### P-test 

$$ \int_{1}^\infty \frac{1}{x^p} \ dx \text{ converges } \iff p > 1$$
We can test cases to see why this works. Consider: 
$$ \int_{1}^b x^{-p} \ dx $$
Case 1: $p \neq 1$

$$ \int x^{-p} = \frac{x^{-p+1}}{-p+1} $$
So 
$$ \int_{1}^b x^{-p} \ dx = \frac{b^{1-p} - 1}{1-p}$$
And now we can look at the limit as $b \to \infty$. 
$$ p > 1 \implies 1 - p < 0 \implies b^{1-p} \to 0 $$
$$ p < 1 \implies 1 - p > 0 \implies b^{1-p} \to \infty $$
So the limit exists and converges if $p  > 1$ 

Now, the case for when $p=1$ 
$$ \int_{1}^b \frac{1}{x} \ dx = \ln b$$
And from the example we know this integral diverges as $b \to \infty \implies \ln R \to \infty$. So $p=1$ diverges too. 

Hence, the only case when the integral converges is when $p > 1$ 
$$\square$$

Another case to consider: 
$$ \int_{0}^1 \frac{1}{x^p} \ dx \text{ converges } \iff p < 1  $$
The proof of this is left as an exercise to the reader
### Other forms 

Another form of an improper integrals is: 
$$  \int_{- \infty}^{\infty} f(x) \ dx $$
In the case above, we can split the integral to get: 
$$ \int_{- \infty}^a f(x) \ dx + \int_{a}^\infty f(x) \ dx $$
And then treat each of them as separate improper integrals. Here's a fun problem, solution to which is give in the notes. Show that: 
$$ \int_{- \infty}^{\infty} \frac{1}{1+x^2} \ dx = \pi$$
### Comparison Test 

When thinking of integrals as areas under curve, if we have 
$$ 0 \leq f(x) \leq g(x) $$
Then the area under $f$ is always under the area of $g$. So if $g$'s area is finite, then $f$'s area must be finite too as $f$ fits under $g$ 

And if $f$'s area is infinite, then $g$'s area must also be infinite. 

So suppose $0 \leq f(x) \leq g(x)$ for all large $x$, then 
$$ \int_{a}^{\infty} g(x) \ dx \text{ converges } \implies \int_{a}^{\infty} f(x) \ dx \text{ also converges}$$
$$ \int_{a}^{\infty} f(x) \ dx \text{ diverges } \implies \int_{a}^{\infty} g(x) \ dx \text{ diverges }$$
Note that the inequality direction matters, i.e. if $f(x) \leq g(x)$ then the convergence of $g \implies$ convergence of $f$, however, the converse tells us nothing. 

Consider the example: 
$$ \int_{1}^\infty \frac{1}{\sqrt{ 1 + x + x^2 }} \ dx $$
Now at first glance, $1 + x + x^2 \sim x^2$, so it might be tempting to consider the comparison with $\frac{1}{x^2}$ 

But it gives us the inequality in the wrong direction, and so comparing bigger function to a convergent function tells us nothing 

# 9.Taylor Series 

The idea behind this is we can approximate a complicated looking function using a polynomial by matching all its derivatives at a point. So we image zooming in on a smooth curve at some point $x=a$ and then if we zoom in enough, the curve looks like a straight line (the tangent) 

3b1b has a good video explaining the intuition behind this. But in terms of approximating, the best polynomial approximation is the one matching all derivatives. So if our polynomial is 
$$P(x) = c_{0} + c_{1}(x-a) + c_{2}(x-a)^2 + \dots $$
And we want this to behave exactly like $f$ around the point $a$, then it must have the same value, slope, and curvature. 

So if we matched the derivatives of all orders, then the polynomial behaves exactly like the function at that point 

Therefore, the general formula for **Taylor** series of $f$ around $x=a$ is: 
$$ f(x) = \sum _{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n$$
When $a=0$, we get the **Maclaurin** series, which is just a special case of the Taylor series and is what given in the notes: 
$$ f(x) = \sum _{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}(x)^n$$
Computing the Taylor series for a function is just a matter of computing derivatives at $x=0$ and then putting that into the formula 

Some common Maclaurin series are as follows:

$$e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!}  =  1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots $$
$$ \sin x = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{(2n+1)!}  =  x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots $$
$$\cos x = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n}}{(2n)!}  =  1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots$$
$$ \ln(1+x)=\sum_{n=1}^{\infty} (-1)^{n-1}\frac{x^n}{n}  =x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots$$


## Cauchy’s Remainder Theorem 

When we build a Taylor polynomial $P_n(x)$, we know the value of $f$, its slope and curvature, etc. up to the $n$th derivative at a point. So the polynomial is perfect at the expansion point. But the moment we move away, the question then turns into an error approximation one, which is where the remainder theorem comes in 

Geometrically, the first way the function can differ from our polynomial is through the $(n+1)$th derivative so up until the expansion point, the error function has $n+1$ zeroes. And the simplest function with $(n+1)$ zeroes at $0$ is: $x^{n+1}$. 

Therefore we know that the error function must look like: $\text{something }\times \ x^{n+1}$ 
And that 'something' is the $(n+1)$ derivative at some point in between by the MVT logic 

It's important to know that we're not saying that the error happens at some random point, but rather that the average behaviour of the $n+1$ derivative controlst he error. 

So the remainder theorem is given by: 

$$ R_{n+1}(x) = \frac{f^{n+1}(c)}{(n+1)!}x^{n+1} $$

### Bounding the error 

Bounding just means we don't know the exact value, but we know it cannot be bigger than some value, say $M$ 

So in our case, we don't know what this value of $c$ is, but we know know how big the derivative can get via properties of the functions. So we instead bound the error: 
$$ |  R_{n+1}(x)| \leq \frac{M}{(n+1)!}|x|^{n+1}, \quad M = \max |f^{n+1}(x)| $$
So this essentially gives us a max possible error, which basically means that no matter what, the error cannot be worse than this 



# 10. Differential Equations 

A differential equation is just a rule that tells us how a function changes, rather than what it is. So instead of $y = x^2$, we have: $\frac{dy}{dx} = 2x$ 

So am ODE describes a family of curves, and when we solve one, we are reconstructing the curve(s) which is consistent with the given rate of change 

The order is the highest derivative present 

[[Tags/Definition\|Definition]]

A **general solution** of an ODE is the most general function $y = f(x)$ that satisfies the ODE And if we want to specify the set of solutions, we can do it with **initial** or **boundary** conditions 

An **initial value problem (IVP)** is an ODE together with an initial condition. A **boundary value problem (BVP)** is an ODE with boundary conditions 

## First order ODEs

An first order ODE has the general form: 
$$\frac{dy}{dx} = f(x,y) $$
It's important to not that there isn't a single method to solving all DEs, the method depends on the structure of the function  

A **linear** first order DE has the form: 
$$ \frac{dy}{dx} + p(x) y = q(x)$$

A DE is **homogeneous** if: 
$$ \frac{dy}{dx} + p(x) y = 0 $$
There are no external forces acting, so this is always separable 

A DE is **non-homogeneous** if:

$$ \frac{dy}{dx} + p(x) y = q(x)$$
Notice that the RHS term is not $0$, so this will requires us to use integration factor method 

### Separation of Variables 

A first order DE is separable if it can be arranged into: 
$$ g(y) \frac{dy}{dx} = h(x) $$
the idea here is that we can 'separate' all the $y$ and the $x$ dependencies 

The derivative represents the change in $y$ per change in $x$, so if the DE splits cleanly into a function of $y$ times a function of $x$, then we can accumulate changes on each side independently to get: 
$$ g(y) dy = h(x) dx$$
Note: derivatives are NOT fractions, this is just using the chain rule backwards 

The method of separation of variables is fairly simple, we rearrange to isolate the $x$ and $y$ terms: 
$$ g(y) dy = h(x) dx$$
And then integrate both sides 
$$ \int g(y) \ dy = \int h(x) \ dx + c $$

## Integration factor 

The problem we want to solve here is: 
$$ \frac{dy}{dx} + p(x) y = q(x)$$
The LHS is almost the derivative of a product, but not exactly, so we'll want to turn it into $\frac{d}{dx} \text{something}$ because derivatives or produces are easy to integrate. The notation used below is slightly different to used in notes, but the idea is the smae. 

The product rule says:

$$\frac{d}{dx}(\mu y) = \mu \frac{dy}{dx} + \mu' y$$

We want this to match:

$$\frac{dy}{dx} + p(x)y$$
  
So we choose $\mu(x)$ such that:

$$\mu'(x) = \mu(x)p(x)$$

This is a tiny DE whose solution is:

$$\mu(x) = e^{\int p(x)\,dx}$$

And the function $\mu(x)$ is called the integrating factor.

So given: 

$$\frac{dy}{dx} + p(x)y = q(x)$$
The steps to solving this: 
 
Compute:  
$$\mu(x) = e^{\int p(x)\,dx}$$
Multiply the entire equation by $\mu(x)$
The LHS  becomes:  
$$\frac{d}{dx}(\mu y)$$
Integrate:  
$$\mu y = \int \mu q(x)\,dx + C$$
Solve for $y$

## 2nd order constants coefficient ODEs 

A second-order differential equation involves the second derivative:

$$y'' = \frac{d^2y}{dx^2}$$
For $a y'' + b y' + c y = 0,$ we look for solutions of the form:
$$y = e^{rx}$$
The exponential function appear here because:
- derivatives of $e^{rx}$ are multiples of itself
- this turns the DE into an algebraic equation

### Characteristic equation: 

When we substitute $y = e^{rx}:$

$$y' = r e^{rx}, \quad y'' = r^2 e^{rx}$$
We get: 

$$a r^2 e^{rx} + b r e^{rx} + c e^{rx} = 0$$

Factor out $e^{rx} \neq 0$:
$$a r^2 + b r + c = 0$$

This quadratic is called the characteristic equation. So solving the DE reduces to solving a quadratic equation.

Now we can have 3 cases for the equation: 

#### Case 1: Two distinct real roots: 

$$ y = Ae^{r_{1}x} + Be^{r_{2}x} $$
#### Case 2: Repeated real root 
$$ y = (A+Bx)e^{rx} $$
The extra $x$ is because $e^{rx}$ alone is not sufficient to generate two independent solutions, so multiplying by $x$ creates that linear independence 

#### Case 3: Complex roots: 
$r = \alpha \pm \beta i$
$$  y = e^{\alpha } (A \cos \beta x + B \sin \beta x)$$

### Non-homogeneous equations: 

For $a y'' + b y' + c y = f(x)$
We write: $y = y_h + y_p$

where: 
- $y_h$: homogeneous solution
- $y_p$: one particular solution

The homogeneous part gives the natural behaviour and the particular part accounts for forcing.

The reason we can split this might seem quite familiar. As linear operators satisfy:
$$L(y_1 + y_2) = L(y_1) + L(y_2)$$
We can see that: 
- homogeneous solutions form a vector space
- adding one forced solution shifts the whole space

This is the same linearity idea we’ve seen in linear algebra.

So the steps are as follows: 

Find the general solution of the associated homogeneous ODE which is called the **complementary function (CF)**
Find any solution to the full non-homogeneous ODE which is called the **particular integral (PI)**
Then the general solution is $y = CF + PI$ 

### Trial Functions for Particular Integrals 

- Linear function $\rightarrow \ \ ax + b$ 
- Quadratic function $\rightarrow \ \ ax^2 + bx + c$ 
- Trig function involving $\cos px$ and/or $\sin px \rightarrow \ \ a \cos px + b \sin px$
- Exponential involving $e^px \rightarrow \ \ ae^{px}$ 
- Sum of functions $\rightarrow$ sum of matching functions 

Note that if a trial function has the same form as part of the complementary function, multiply the trial function by $x$ to form a new trial function 


### Optional Asides: 

Where is e coming from when finding complementary functions? 

https://math.stackexchange.com/questions/764171/proof-that-ex-is-the-eigenvector-of-the-derivative-operator




































































































































































































































































































































































