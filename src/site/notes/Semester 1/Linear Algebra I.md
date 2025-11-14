---
{"dg-publish":true,"permalink":"/semester-1/linear-algebra-i/"}
---


# Link back to [[Semester 1/Home page\|Home page]]
# [Link to typed notes: ](https://blackboard.soton.ac.uk/ultra/courses/_233978_1/outline/edit/document/_7502405_1?courseId=_233978_1&view=content&state=view)

# 0. Complex Numbers 
$$ \mathbb{C} = \{  a+bi \mid a,b \in \mathbb{R}  \} $$
$$ \mathrm{Re}(a+bi) = a$$
$$\mathrm{Im}(a+bi) = b$$
### Why is i on the other side?? 

Graphically, $z = a+bi \in \mathbb{C}$ corresponds to the point $(a,b) \in \mathbb{R^2}$

[[Tags/Definition\|Definition]] Modulus of a complex number $a+bi$ is 

$$ \mid z \mid = \sqrt{a^2+b^2} $$
Think of it like vectors and distances from origin 

[[Tags/Definition\|Definition]] Argument of a complex number is the angle between $z$ and the positive $x$ axis measured in radians anti-clockwise 

$Arg(z)$ is the principle value of the argument, but $arg(z)$ is defined by adding + $2\pi n$

The argument lies in the interval $(-\pi, \pi]$ : not including $-\pi$ but including $\pi$

$$ e^{i\theta} = cos\theta + i\sin\theta , \space \theta \in \mathbb{C}$$
 
## Polar form

Every non-zero complex number can be written in the form of 
$$ z = r (\cos\theta + \sin\theta) = re^{i\theta} $$
Where 

$r = \mid z \mid, \space \theta = arg(z)$

Let $z_1$ be $r_1 e^{i \theta_1}$ and $z_2$ be $r_2 e^{i \theta_2}$

### Multiplication 

$$z_1 z_2 = (r_1 r_2) e^{i ( \theta_1 + \theta_2)}$$

### Division 
$$\frac{z_1}{z_2} = (\frac{r_1} {r_2}) e^{i ( \theta_1 - \theta_2)}$$

### Powers (De Moivre's)
$$ (r (\cos \theta + i \sin \theta))^n = r^n (\cos n \theta + i \sin n \theta) $$ 

$$z^n = (re^{i \theta})^n = r^n e^{in \theta}$$

### Roots of units 

$$ z^\frac{1}{n} = r^\frac{1}{n} e^{i \frac{(\theta + 2k \pi)}{n}}, \space k = 0, 1, ... n-1 $$

### Example 

Take $z = 1+ i$

- Modulus = $\mid z \mid = \sqrt{1^2 + 1^2} = \sqrt2$
- Argument = $Arg(z) = \arctan(1) = \frac{\pi}{4}$$
- Polar form: $z = \sqrt2 (\cos \frac{\pi}{4}  + i \sin \frac{\pi}{4})$
- Exponential form: $\sqrt2 e^{\frac {i \pi} {4} }$

## Conjugates and Reciprocals 

### Why do they matter? 

- Getting rid of the $i$ in the denominator 
	- Long-standing convention that we want denominator to be real numbers 
	- Modulus and argument can be easily seen 
- Calculating the magnitude 
	- $\mid z \mid
{ #2}
 = z \bar{z}$
- Later - calculating products in vector spaces 
- Roots of real polynomials as they come in conjugate pairs 
---

If $z = a+bi$ , the conjugate is defined as: $\bar{z} = a-bi$ 
- This is essentially reflecting $z$ is the real axis 

- If $z = r e^{i \theta}$  then $\bar{z} = r e ^{-i \theta}$ $$ z \bar{z} = \mid z \mid
{ #2}
$$
To think about the point above geometrically, $z$ and $\bar{z}$ are just two vectors which have the same magnitude but one of the reflection of the other in the real axis, so if we multiply those two vectors, we are essentially doubling the magnitude of the vector. This also makes intuitive sense in polar form 
$$ z^{-1} z = 1 $$
The reciprocal by definition is the number that when multiplied to gives the result of $1$ 
In terms of geometry, $z$ is essentially scaling a vector by $r$ and rotating it by $\theta$, and what $z^{-1}$ does is scales the vector by $\frac{1}{r}$ and rotates it by $-\theta$

## Reciprocals: $z^{-1} = \frac{\bar{z}}{\mid z \mid
{ #2}
}$

Proof:

Let $z = a+ bi$ 

We want $z^{-1} = \frac{1}{z}$

Therefore: 

$$  \frac{1}{z} = \frac{1}{a+bi} \times \frac{a-bi}{a-bi} = \frac{a-bi}{a^2 + b^2}$$


The conjugate $\bar{z} = a-bi$

And the modulus is $\mid z \mid = \sqrt{a^2 + b^2}$
Therefore $$ z^{-1}=  \frac{\bar{z}}{\mid z \mid
{ #2}
} , \space z \neq 0$$

### Reciprocals in polar form 
Any non-zero complex number can be written as: 

$$ z = re^{i \theta} $$

The reciprocal $z^{-1}$ can be written as: 

 $$z^{-1} = \frac{1}{z} = \frac{1}{re^{i \theta}} = \frac{1}{r} \times \frac{1}{e^{i \theta}} $$
 But $\frac{1}{e^{i \theta}} = e^{-i \theta}$

 So we have
$$ z^{-1} = \frac{1}{r} e ^{-i \theta} $$

This form can also be derived from the earlier formula: $z^{-1} = \frac{\bar{z}}{\mid z \mid
{ #2}
}$

We have $\bar{z} = re^{-i \theta}$ and $\mid z \mid
{ #2}
 = r^2$

$$\frac{\bar{z}}{\mid z \mid
{ #2}
} = \frac{re^{-i \theta}}{r^2} = \frac{1}{r} e^{-i \theta}$$

Polar form is very useful when converting numbers from their cartesian form to mod-arg form 

If we had $z = a+ bi$, we would have to expand a product, deal with conjugates and end up with fractions for both real and imaginary parts. 

But if we had reciprocals in polar form with $z = re^{i \theta}$, then we just need to invert the modulus and flip the angle 

Consider this example: $z = 3+4i$

- Cartesian way: 

$$z^{-1} = \frac{3-4i}{3^2 + 4^2} = \frac{3}{25} - \frac{4}{25}i$$

And now consider the polar way: 

$r = 5, \space \theta = \arctan(\frac{4}{3})$

$$z^{-1} = \frac{1}{5} e ^{-i \theta}$$
## 
Proof of fundamental theorem of algebra here 
- Need intermediate value theorem to prove stuff 

### Roots and conjugate pairs 

If a polynomial has real coefficients, then any non-real complex root must appear with its complex conjugate as another root 

So if $a+bi, b \neq 0$ is a root, then $a-bi$ is also a root 
Why? 

Suppose the polynomial is 
$$ P(x)= a_n x^n + a_{n-1} x^{n-1} + … + a_1 x + a_0 , \space a_k \in \mathbb{R},  $$
Now assume that $z \in \mathbb{C}$ is a root: 

$$ P(z) = a_n z^n + a_{n-1} z^{n-1} +... + a_1 z + a_0 = 0 $$
This is essentially saying that if we plug is $z$ which is in the set of complex numbers into $P(z)$, the result is 0, which means $z$ is a solution to the polynomial 

Then if we take the conjugate of both sides: 
$$ \bar{P(z)} = \bar{0} $$
However, $\bar{0} = 0$

And because the coefficients are real: 

$$ \bar{{P(z)}} = a_n \bar{z}^n + a_{n-1} \bar{z}^{n-1} +... + a_1 \bar{z} + a_0 = P(\bar{z}) $$
So we've shown that $$ P(\bar{z}) =0 $$
Hence, if $z$ is a root, so is $\bar{z}$

### Solving roots in polar form 


---

# 1. Real $n$ space $\mathbb{R}^n$

[[Tags/Definition\|Definition]] The real n-space $\mathbb{R}^n$ is the collection of n-tuple of real numbers 

$$ \underline{v} = (x_1, x_2, … , x_n) , \space \forall x_i \in \mathbb{R} $$

Eg: 
$\mathbb{R}^0$ = a single point 
$\mathbb{R}^1$ = the real number line 
$\mathbb{R}^2$ = the plane 
Etc… 

$\mathbb{R}^n$ can also be viewed as set of points 

## Scalar/Dot product 

A scalar product (aka dot product) of two vectors returns a scalar (i.e a real or a complex number)

For $\underline{u} = (u_1, u_2, … u_n)$ and $\underline{v} = (v_1, v_2… v_n)$ in $\mathbb{R}^n$, we define 
$$ \underline{u} \cdot \underline{v} = u_1 v_1 + u_2 v_2 + … + u_n v_n = \sum_{i=1}^{n} u_i v_i $$
### Properties of scalar product 
- Commutative 
- Distributive 


[[Tags/Definition\|Definition]] Orthogonal vectors - vectors at right angles 
$$ \vec{a} \cdot \vec{b} = 0 $$
## Norm of a vector 

Norm is basically the magnitude or length of a vector 

$$ || \vec{v} || = \sqrt{\vec{v} \cdot \vec{v}} $$

Unit vector - A vector with the magnitude of 1 

$$ \hat{a} = \frac{\vec{a}}{||\vec{a}||} $$

Generalized Pythagoras theorem: 

$$ || \vec{a} + \vec{b} ||
{ #2}
 = ||\vec{a} || + ||\vec{b} ||$$ 
## Projections  

Intuitively, imagine we have two vectors: $\vec{a}$ and $\vec{b}$, and we want to know how much of $\vec{a}$ lies in the direction of $\vec{b}$ . 

The **projection** of a vector $\vec{a}$ onto another vector $\vec{b}$ is the "shadow" of $\vec{a}$ in the direction of $\vec{b}$. It tells you how much of $\vec{a}$ lies along $\vec{b}$. 

Now, the problem is, $\vec{a}$ might not lie perfectly along $\vec{b}$, it might be slanted, so we want to find the part of $\vec{a}$ that does lie along it, and that's what projection is. 

We know that any point on the line $\vec{b}$ must look like a multiple of $\vec{b}$. So every point on that line can be written as: 

$$ \vec{b} = \lambda {\vec{b}}$$
We need to find a $\lambda$ multiple of $\vec{b}$ gives the point on that line where $\vec{a}$ drops a perpendicular, so we need a scalar $\lambda$ such that the point $P$ on the line through $\vec{b}$ satisfies the equation: 
$$ \vec{OP} = \lambda b $$
and the vector from $P$ to the tip of $\vec{a}$ (which is $a- \lambda b)$ is perpendicular to P 

Since perpendicular vectors have dot product = 0, we have 

$$ ( \vec{a}- \lambda \vec{b}) \cdot{\vec{b}} = 0 $$
$$ \vec{a} \cdot \vec{b} - \lambda \vec{b} \cdot \vec{b} = 0 $$
$$ \lambda = \frac{\vec{a} \cdot \vec{b}}{\vec{b} \cdot \vec{b}} $$

Therefore, the **component** of $\vec{a}$ along $\vec{b}$ is the scalar $\frac{\vec{a} \cdot \vec{b}}{|\vec{b}|^2}$, and the **projection** is vector $\lambda \vec{b}$

## Cauchy-Schwarz Inequality 


Using the dot product definition, we have 
$$ \vec{a} \cdot \vec{b}  = |\vec{a}| |\vec{b}| \cos \theta $$
Since $\cos \theta \leq 1$, we immediately get: 
$$  | \vec{a} \cdot \vec{b}| \leq |\vec{a} ||\vec{b}|$$
This is the Cauchy-Schwarz inequality, and it essentially means that a project (shadow) can never be longer than the actual vector. 

## Triangle inequality 

The triangle inequality here below can be proved using the Cauchy-Schwarz inequality: 

$$ |\vec{a} + \vec{b} |^2 = |\vec{a}|^2 + 2(\vec{a} \cdot \vec{b}) + |\vec{b}|^2$$
After expanding the LHS, we can how apply the Cauchy-Schwarz inequality 
$$  | \vec{a} \cdot \vec{b}| \leq |\vec{a} ||\vec{b}|$$
So we have 

$$ |\vec{a} + \vec{b} |^2 \leq |\vec{a}|^2 + |\vec{a}| |\vec{b}| + |\vec{b}|^2 = (|\vec{a}| + |\vec{b}|)^2 $$
After taking square roots, we have: 

$$ | \vec{a} + \vec{b} | \leq |\vec{a}| + | \vec{b}| $$

## Equation of a Line in $R^n$

To define a line, we need two things (maybe more, but two main): 
- A point the line passes through, called the **position vector** or the point of origin of the line. Call it $\vec{a}$. So if the line passes through a point $A(x_1, y_1, z_1)$ then $\vec{a} = (x_1, y_1, z_1)$

- A direction the line travels in, called the **direction vector**. Call it $\vec{d}$ 

There are a few ways to describe lines. 
### Vector equation 

The vector equation of a line is the most geometric form, if the line passes through the point $A$ and is parallel to the direction of vector $\vec{d}$, then every $r$ on the line can be reached by: 

$$ \vec{r} = \vec{a} + \lambda \vec{d} $$

where $\lambda$ is a scalar that moves along the line. Intuitively, we're starting at $\vec{a}$ and then moving in direction $\vec{d}$ for some distance $\lambda$ 

### Parametric equation 

This is just a component form of the vector equation, but it's useful when working with intersections or substituting into other equations for $\lambda$. 

$\lambda \in \mathbb{R}$ is essentially the parameter controlling position along the line (and yes that's why it's parametric)

If we write vectors in components: 
$$ \vec{a} = (x_1, y_1, z_1), \space \vec{d} = (a,b,c), \space \vec{r} = (x,y,z) $$
Then 
$$ (x,y,z) = (x_1,y_1,z_{1}) + \lambda(a,b,c) $$
This gives 

In this case, the parametric equation of a line is: 

$$x = x_{1} + a \lambda $$
$$y = y_{1} + b \lambda $$
$$z = z_{1} + c \lambda $$

### Cartesian equation 

The cartesian form eliminates $\lambda$ and expresses the relation between $x,y,z$. It's also useful when finding where two lines/planes intersect. 

### Converting from parametric to Cartesian equation example  

When converting from parametric to cartesian, our goal is to eliminate $\lambda$

So given our three parametric equations above, we can solve each of them for $\lambda$ to get our cartesian equation of a line, which in general form is: 

$$ \frac{x-x_{1}}{a} = \frac{y-y_{1}}{b}= \frac{z-z_{1}}{c}$$

Geometrically speaking, we get a ratio of how much we've moved along the line (scaled by $\lambda$) in each coordinate direction 
### Parallel, Intersection, Skew 

In $\mathbb{R}^2$, lines are either parallel or their intersect at a point. But in $\mathbb{R}^3$, lines can either be parallel, intersect, or skew, or coincident. 

It's useful to outline what each of them mean and what their test would look like: 

[[Tags/Definition\|Definition]]

- **Coincident** - the direction vectors are multiple of each other as one point satisfies the other line's equation
	- The points lie on the same line 
- **Parallel** - direction vectors are multiples, but there is no common point 
	- The lines are in the same direction, but different positions
- **Intersecting** - system has a single consistent solution for the parameters ($\lambda, \mu$)
	- The lines meet a single point 
- **Skew** - system has no solutions (inconsistent equations)
	- Not parallel, never meet 
	- Lie in different planes 

#### Forming and solving systems of equations to determine the arrangement of lines in $\mathbb{R^3}$

Let the two lines $L_1$ and $L_2$ be given by: 

$$  L_1 : \vec{r} = \vec{a_{1}} + \lambda \vec{d_{1}}$$
$$  L_1 : \vec{r} = \vec{a_{1}} + \lambda \vec{d_{2}}$$
where 
- $\vec{a_{1}}, \vec{a_{2}} \in \mathbb{R}^3$ are position vectors of points on each line. 
- $\vec{d_{1}}, \vec{d_{2}} \in \mathbb{R}^3$ are the direction vectors 
- $\lambda, \mu \in \mathbb{R}^3$ are scalar parameters

In component form, this gives a system of 3 linear simultaneous equations in the two unknowns $\lambda$ and $\mu$ 

$$x_{1} + a_{1} \lambda = x_{2} + a_{2} \mu $$
$$y_{1} + b_{1} \lambda = y_{2} + b_{2} \mu $$
$$z_{1} + c_{1} \lambda = z_{2} + c_{2} \mu $$
And we we can either 
- Eliminate one parameter 
- Use the determinant of matrix (more on this later)
- Substitute using pairs of equations

Once we have our result, we can use our definitions to check the arrangement of lines in $\mathbb{R}^3$

- We can only have a unique point of intersection if the system has a unique consistent solution for $\lambda, \mu$
- If the system has no solution and are not parallel, they are skew - i.e. lie in different planes 

## Equation of a plane 

Let's start with the intuition, what is a plane? (Yes it is something that flies..)

A **plane** is a flat 2D surface that extends infinitely in three dimensions. We can think of it as : 
- The set of all points that satisfy one linear condition in $x, y, z$ 
- Or, all points that we can reach starting from one point and moving along two independent direction vectors 

[[Tags/Definition\|Definition]] A plane can be defined by a point $a$ that lies on it, and a **normal vector** $n$ that is perpendicular to the plane 

### Vector equation 

So a plane is a set of all points $\vec{r} = (x,y,z)$ such that the vector $(\vec{r} - \vec{a})$ lies orthogonal (or perpendicular) to $n$

so if $\vec{r} = (x,y,z)$ is a general point on the plane, then we have 
$$ \vec{n} \cdot (\vec{r} - \vec{a}) = 0 $$
Check that this makes sense, the dot product being zero means that the vectors are perpendicular 

### Cartesian equation 

Say the normal vector $\vec{n} = (A,B,C)$ and $\vec{a} = x_{0}, y_{0}, z_{0}$, then after computing the dot product and simplifying

$$ Ax + By + Cz + D = 0$$
Where $D = -(Ax_{0} + By_{0} + Cz_{0})$
Also note that $$ \vec{r} \cdot \vec{n} = \vec{a} \cdot \vec{n} $$

Intuitively, this equation defines all the points $(x,y,z)$ that live in a plane tilted such that its perpendicular points in the direction of $(A,B,C)$ 

There are pretty good 3b1b videos on Linear Algebra for some visual understanding. I often imagine solving problems in Grant Sanderson's voice to give myself some confidence when approaching questions 

### Parametric equation  

As with lines, planes can also be defined using a point and two non-parallel direction vectors 

So if $a$ is a point on the plane, and $b$ and $c$ are two independent direction vectors lying in the plane, then any point on the plane can be written as: 

$$ \vec{r} = \vec{a} + \lambda \vec{b}  + \mu \vec{c}$$
And every point on the plane is reachable by some combination of $\lambda$ and $\mu$ 

## Vector product 

To find perpendicular/orthogonal vectors, we need to have something that lets us calculate that, and this is where the vector product comes in. The ’trick’ so to speak of calculating this is similar to finding determinants in matrices

Let 

$$

\mathbf{a} = 

\begin{pmatrix}

a_1 \\ a_2 \\ a_3

\end{pmatrix}

\quad \text{and} \quad

\mathbf{b} =

\begin{pmatrix}

b_1 \\ b_2 \\ b_3

\end{pmatrix}

$$

be two vectors in $\mathbb{R}^3$.

The **vector product** $\mathbf{a} \times \mathbf{b}$ is the vector in $\mathbb{R}^3$ with coordinates

$$

\mathbf{a} \times \mathbf{b} =

\begin{pmatrix}

a_2b_3 - a_3b_2 \\

a_3b_1 - a_1b_3 \\

a_1b_2 - a_2b_1

\end{pmatrix}.
$$
### Vector product properties 

- Vector products are NOT communicative and NOT associative 

When we take the cross product $\vec{a} \times \vec{b}$, we get a new vector that's orthogonal to both $\vec{a}$ and $\vec{b}$ . It's magnitude is given by: 
 $$| \vec{a} \times \vec{b}| = |\vec{a}| |\vec{b}| \sin \theta $$
#### Parallelograms... 
Where $\theta$ is the angle between $\vec{a}$ and $\vec{b}$. This is also the area of a parallelogram formed by the two vectors. And the direction of the cross product is orthogonal to the parallelogram. 

Given that there are two directions to a plane, up and down, we need to know which direction the cross product points towards. And this is where the right hand rule comes in. 

- If we point the index finger along vector $\vec{a}$
- The middle finger along vector $\vec{b}$ which is at right angles to $\vec{a}$
- Then our thumb now points in the direction of $\vec{a} \times \vec{b}$

Now, if we flip the order, and instead do $\vec{b} \times \vec{a}$, the magnitude remains the same, but the direction reverses 

So we get: 
$$\vec{a} \times \vec{b} = -\vec{b} \times \vec{a}$$

Geometrically speaking, the cross product represents the oriented area of the parallelogram spanned by $\vec{a}$ and $\vec{b}$. 

## Intersection of Lines and Planes in $\mathbb{R}^3$ 

There are 3 cases for an intersection between a line and a plane: 
- No intersection - $L$ is parallel to $\pi$
- Infinitely many points - $L$ is contained in $\pi$ 
- One point $L$ intersects $\pi$ in a single point 

The first two cases are pretty straightforward. And the final case can be checked by computing the normal vector to $\pi$ and seeing if it’s orthogonal to the direction of $L$. 

Now, the intersection of 3 planes in $\mathbb{R}^3$ has 4 possibilities:

- The intersection is a single point 
- The intersection is a line (star)
- The intersection is another plane when all planes coincide 
- The intersection is empty (at least two planes are parallel or they form a prism)

## Distances in $\mathbb{R}^3$ 

### Point and a Plane 

Given a point $P$ and a plane $\pi$ in $\mathbb{R}^3$, we want to find the shortest distance between a plane and a point 

Say if we've got a plane: 

$$ \vec{n} \cdot (\vec{r} - \vec{a}) = 0$$
and a point $P$ with position vector $\vec{p}$

Then the distance from $P$ to the plane is the projection of $(\vec{p} - \vec{a})$ onto the normal $\vec{n}$ : 

$$ d = \frac{|\vec{n} \cdot (\vec{p} - \vec{a})|}{|\vec{n}|}$$
Imagine standing above a plane with a flashlight pointing along the normal vector. Then the shadow of the position vector onto that normal is the perpendicular, i.e the shortest path. 

### Point and a line 

Let's say we want to find the distance between the line $L: R = A + \lambda \vec{a}$ and the point $P$, both in $\mathbb{R}^3$

Use Pythag, we can show that the distance between $P$ and $L$ is equal to the $|\vec{PN}|$ where $\vec{N}$ is the point such that $\vec{PN}$ is perpendicular to $\vec{a}$

We can do this by considering projections. The projections of $\vec{PA}$ along $\vec{a}$ is 

$$ proj_{a}(\vec{PA}) = \frac{(\vec{PA} \cdot \vec{a})}{(\vec{a} \cdot \vec{a})}a$$
The $\vec{PA}$ here is made up of two parts, the parallel part (projection) and the perpendicular part. So to get the perpendicular component, we have to subtract the projection: 
$$ \vec{PN} = \vec{PA} - proj_{a}(\vec{PA})$$

The distance is therefore given by the norm or the magnitude of both sides 
$$ ||\vec{PN}|| = || \vec{PA} - \frac{(\vec{PA} \cdot A)}{\vec{a} \cdot \vec{a}}a|| $$

---

# 2. Matrix Algebra 

## Definitions 

[[Tags/Definition\|Definition]] Suppose that $m, n \in \mathbb{N}$ are natural numbers. 
An $m \times n$ matrix $A$ is a rectangular array with $m$ rows and $n$ columns:

$$
A =

\begin{pmatrix}

a_{11} & a_{12} & \cdots & a_{1n} \\

a_{21} & a_{22} & \cdots & a_{2n} \\

\vdots & \vdots & \ddots & \vdots \\

a_{m1} & a_{m2} & \cdots & a_{mn}

\end{pmatrix}.
$$

The coefficients $a_{11}, a_{12}, \dots, a_{mn}$ are called the **entries** of the matrix. 
For any $i \in \{1, \dots, m\}$ and $j \in \{1, \dots, n\}$, the entry $a_{ij}$ is said to be the $(i,j)$-th element (or the $(i,j)$-th entry) of $A$.  

$(A)_{ij}$ Is used to denote $a_{ij}$. 

[[Tags/Definition\|Definition]] **Zero matrix** 
Size $m \times n$ matrix in which all entries are $0$.

[[Tags/Definition\|Definition]] **Diagonal matrix** 
A square matrix $A$ is diagonal if $a_{ij} = 0$ whenever $i \neq j$ 
(i.e., all non-diagonal entries are zero):
$$
A =

\begin{pmatrix}

a_{11} & 0 & \cdots & 0 \\

0 & a_{22} & \cdots & 0 \\

\vdots & \vdots & \ddots & \vdots \\

0 & 0 & \cdots & a_{nn}

\end{pmatrix} $$
[[Tags/Definition\|Definition]] **Identity matrix** 
An $n \times n$ diagonal matrix with $1$'s on the diagonals. Denoted by $I_n$

$$

I_n =

\begin{pmatrix}

1 & 0 & \cdots & 0 \\

0 & 1 & \cdots & 0 \\

\vdots & \vdots & \ddots & \vdots \\

0 & 0 & \cdots & 1

\end{pmatrix}_{n \times n}

\ $$

Thus $I_n = (\delta_{ij})$, where

$$

\delta_{ij} = 

\begin{cases}

1, & \text{if } i = j, \\

0, & \text{if } i \neq j.

\end{cases}
$$

The addition and subtraction for matrices is only defined for matrices of the same size, but multiplication, as well will see below, has other properties 

Why can’t we add or subtract matrices that aren’t the same size?? 
## Matrix multiplication 

Let $A$ be an $m \times n$ matrix and $B$ be a $n \times p$ matrix. 

then $C = AB$ is the $m \times p$ matrix defined as: 

$$ c_{ij} = \sum_{k=1}^{n} a_{ij}b_{kj} $$
The matrix product is essentially the product of the row vectors in $a$, and the column vectors in $b$. So it works like a dot product. 
$$

C = AB =

\begin{pmatrix}

a_1 \cdot b_1 & a_1 \cdot b_2 & \cdots & a_1 \cdot b_p \\

a_2 \cdot b_1 & a_2 \cdot b_2 & \cdots & a_2 \cdot b_p \\

\vdots & \vdots & \ddots & \vdots \\

a_m \cdot b_1 & a_m \cdot b_2 & \cdots & a_m \cdot b_p

\end{pmatrix}_{m \times p} $$
So, $c_{ij} = a_i \cdot b_j$, the $(i,j)$-th entry of $AB$ is equal to the scalar product of the $i$-th row of $A$ with the $j$-th column of $B$ 
So the product $AB$ is only defined if the number of columns in $A$ equals the number of rows in $B$ 

### Properties: 
- Distributivity 
- Associativity 
## Transposition of a Matrix 

Let $A = (a_{ji})$ be an $m \times n$ matrix. The transpose of $A$ is the $n \times m$ matrix $A^T$ defined by

$$
(A^T)_{ij} = (A)_{ji} = a_{ji}, \quad \text{for all } i, j, \ 1 \leq i \leq n, \ 1 \leq j \leq m.
$$

$$ A =

\begin{pmatrix}

a_{11} & a_{12} & \cdots & a_{1n} \\

a_{21} & a_{22} & \cdots & a_{2n} \\

\vdots & \vdots & \ddots & \vdots \\

a_{m1} & a_{m2} & \cdots & a_{mn}

\end{pmatrix}_{m \times n}

\quad \text{then} \quad

A^T =

\begin{pmatrix}

a_{11} & a_{21} & \cdots & a_{m1} \\

a_{12} & a_{22} & \cdots & a_{m2} \\

\vdots & \vdots & \ddots & \vdots \\

a_{1n} & a_{2n} & \cdots & a_{mn}

\end{pmatrix}_{n \times m}.$$

In other words, rows of $A$ become columns of $A^T$, and columns of $A$ become rows of $A^T$.

Example: 

$$ \quad

\begin{pmatrix}

1 & 2 & 3 \\

4 & 5 & 6

\end{pmatrix}^T

=

\begin{pmatrix}

1 & 4 \\

2 & 5 \\

3 & 6

\end{pmatrix}, \quad

\begin{pmatrix}

1 & 2 & 3 \\

4 & 5 & 6 \\

7 & 8 & 9

\end{pmatrix}^T

=

\begin{pmatrix}

1 & 4 & 7 \\

2 & 5 & 8 \\

3 & 6 & 9

\end{pmatrix}. $$

If $A = A^T$, then the matrix $A$ is said to be symmetric

### Properties

- $(A^T)^T = A$  - Flipping twice returns the original matrix 
- $(A+B)^T = A^T + B^T$ - Transposing a sum is the same as sum of the transposes 
- $(kA)^T = kA^T$ - a scalar doesn't affect a transpose 
- $(AB)^T = B^T A^T$ - when we flip a product, we reverse the roder 

## Inverse of a Matrix 

For numbers, the inverse "undoes" the effect. Eg: $$ 3 \times \frac{1}{3} = 1 $$
For matrices, the inverse works in the same way, it undoes the transformation a the matrix does: 
So $$ AA^{-1} = I$$
Where $I$ is the identity (the "do nothing") matrix 

- Only square matrices can inverted, but not all square matrices are invertible  
- An inverse exists iff $det(A) \neq 0$ 

An $n \times n$ matrix $A$ is said to be invertible if there exists an $n \times n$ matrix $B$ such that

$$

AB = I_n \quad \text{and} \quad BA = I_n,

$$

 where

$$

I_n =

\begin{pmatrix}

1 & 0 & \cdots & 0 \\

0 & 1 & \cdots & 0 \\

\vdots & \vdots & \ddots & \vdots \\

0 & 0 & \cdots & 1

\end{pmatrix}

$$

is the $n \times n$ identity matrix. In this case, $B$ is called the inverse of $A$, and is denoted $B = A^{-1}$.
Let $A$ be a $2 \times 2$ matrix with $ad - bc \neq 0$.
  $$A =

\begin{pmatrix}

a & b \\

c & d

\end{pmatrix}

$$

 Then $A$ is invertible and
$$

A^{-1} = \frac{1}{ad - bc}

\begin{pmatrix}

d & -b \\

-c & a

\end{pmatrix}. $$

### Properties 
Let $A$ and $B$ be invertible $n \times n$ matrices. Then the following are true: 
- $A$ has a unique inverse 
- $A^{-1}$ is invertible and $(A^{-1})^{-1} = A$ 
- $AB$ is invertible and $(AB)^{-1} = B^{-1}A^{-1}$ 
- $A^T$ is invertible and $(A^T)^{-1}=  (A^{-1})^T$ 


## Powers of a Matrix 

If $A$ is a square matrix ($n \times n$), then we can multiply it by itself: 
$$ A^2 = A \cdot A , \quad A^3 = A \cdot A \cdot A  $$

- If $A$ and $B$ commute, ($AB = BA$) then $(AB)^n = A^n B^n$ 
- $A^{-n} = (A^{-1})^n$ 

# 3. Systems of Linear Equations

A system of $m$ equations in $n$ unknown can be written as: 
And in matrix form:

$A \mathbf{x} = \mathbf{b}$


$$
\begin{pmatrix}

a_{11} & a_{12} & \cdots & a_{1n} \\

a_{21} & a_{22} & \cdots & a_{2n} \\

\vdots & \vdots & \ddots & \vdots \\

a_{m1} & a_{m2} & \cdots & a_{mn}

\end{pmatrix}

\!\!

\begin{pmatrix}

x_1 \\ x_2 \\ \vdots \\ x_n

\end{pmatrix}

=

\begin{pmatrix}

a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n \\

a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n \\

\vdots \\

a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n

\end{pmatrix}.
$$

Where: 
- $A$ = coefficient matrix 
- $\mathbf{x} = (x_{1}, x_{2}\dots x_{n})^T$ - the column vector of variables 
- $\mathbf{b} = (b_{1}, b_{2}\dots b_{m})^T \in \mathbb{R}^m$

## Augmented Matrix 

The augmented matrix of system is 

$$ 
(A \,|\, \mathbf{b}) =

\begin{pmatrix}

a_{11} & \cdots & a_{1n} & b_1 \\

\vdots & \ddots & \vdots & \vdots \\

a_{m1} & \cdots & a_{mn} & b_m

\end{pmatrix}$$

## Row Operations

There are 3 allowed row operations that allows us to simplify systems without changing the solution set. I.e. matrices are are row equivalent 

- Row operation are invertible, i.e. their inverses are also row operations 

### Row Scaling 
$$ R_{i} \rightarrow \lambda R_{i}$$
### Row interchange (swap)
$$ R_{i} \leftrightarrow R_{j}
$$
### Row replacement 
$$ R_{i} \rightarrow R_{i} + \mu R_{j}, \quad i \neq j, \mu \in \mathbb{R}$$

## Gaussian Elimination 

Consider we're trying to solve a system of simultaneous linear equations like 
$$ \begin{cases}
x + 2y - z = 3 \\ 
2x + y + z = 8 \\
-3x + y + 2z = -5
\end{cases}$$
Instead of solving one variable at a time using substitution, we can turn this into an augmented matrix. 

So we instead have: 
$$
\begin{pmatrix}

1 & 2 & -1& 3 \\

2 & 1 & 1 & 8 \\

-3 & 1 & 2 & -5

\end{pmatrix}
$$
So each row is an equation, and each column, except the last one, is one variable's coefficients. 

The idea now is to use the row operations listed above to reduce the augmented matrix to **row echleon form (REF)** or **reduced row echleon form (RREF)**

A **pivot** is the first non-zero entry in a row of a matrix 

A matrix is is REF if: 
- Every **pivot** is to the right of all pivots above it 
- Zero rows are at the bottom 

A matrix is in RREF if: 
- It’s already in REF 
- Every pivot is $1$ 
- Every column containing a pivot has all entries equal to $0$ 

[[Tags/Definition\|Definition]] Gaussian Elimination is the method of solving linear equations by starting with $(A \,|\, \mathbf{b})$ and performing row operations to put $A$ into RREF, then reading the solutions . 

Each row in the matrix represents a plane in 3D (or a line in 2D or a hyperplane in higher dimensions). So Gaussian elimination is essentially rotating and scaling these planes until they're "aligned with the axes". The intersection point doesn't change, we just manipulate it to make it easier to understand

### Reading solutions 

Once our matrix is in REF, the augmented matrix will correspond to the solutions of the equation 

$$

\begin{pmatrix}
1 & 0 & 0 & \alpha \\
0 & 1 & 0 & \beta \\
0 & 0 & 1 & \gamma \\
\end{pmatrix}
$$
$$
\begin{pmatrix}
x = \alpha\\
y = \beta\\
z = \gamma
\end{pmatrix}
$$


### Reducing a matrix to RREF 

Our goal is to transform a given matrix $A$ into a version where: 

$$
A{_{RREF}} = \begin{pmatrix}

1 & 0 & 0 &\cdots & * \\
0 & 1 &0 & \cdots & *\\
0 & 0 & 1 & \cdots &  \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0 & 0 & 0 & \cdots & 0
\end{pmatrix}
$$
- Each row starts with a $1$ (pivot) which is to the right of the pivot above it 
- Each pivot column has zeros above and below the pivot 
- Any rows of all zeroes go to the bottom 

The means that: 
- Each pivot correspond to a leading variable

To reduce a matrix to RREF: 
- Starts with the first non-zero column going from left to right - this will be our pivot column 
- If the first entry is non-zero, use that, otherwise, swap that row with one below so that the pivot moves to the top of the block 
- Make the pivot $1$ using row operations 
- Use row operations to make all entries below the pivot = $0$ 
- Now move diagonally (one column to the right and down) and repeat the process until all pivots have zeroes below 
- And go back and make all entries above the pivot zero 

## Matrix inverses using row operations 

[[Tags/Definition\|Definition]] A system of linear equation is **consistent** iff the augmented matrix, when put into this REF has no rows of the form $(0… 0 | b)$ with $b \neq 0$ 

Each matrix has a unique matrix in RREF 

If $A$ is invertible, then there is a unique solution given by $\mathbf{x} = A^{-1} \mathbf{b}$ 

Given any $\mathbf{x}$ with $A\mathbf{x} = \mathbf{b}$ 

$$ \mathbf{x} = I_{n}\mathbf{x} = (A^{-1}A)\mathbf{x} = A^{-1}(A\mathbf{x}) = A^{-1}\mathbf{b}$$

Here, the key idea is that row operations that turn $A$ into $I$ will also turn $I$ into $A^{-1}$.

[[Tags/Definition\|Definition]] **Elementary matrix** - A matrix obtained from the identity matrix $I_n$ by doing **ONE** row operation. Doing row operations is the same as multiplying by elementary matrices. One of the problem sheets goes through this proof 

Each elementary matrix is invertible, and it’s inverse is an elementary matrix of the same type. Ie. if we multiply $E$ by any matrix $A$, we perform that same row operation on $A$. 

If $A$ is an $n \times n$ matrix, then: 
- $A$ is invertible 
- The unique solution to $A \mathbf{x} = \mathbf{0}$ is $\mathbf{x}  = \mathbf{0}$
- The RREF of $A$ is $I_n$ 
- $A$ is a product of $n \times n$ elementary matrices 

If $A$ and $B$ are $n \times n$ matrices and $AB = I_n$, then both $A$ and $B$ are invertible and $A^{-1} = B$ and $B^{-1} = A$ 

### Algorithm for finding inverses using row operations 

Suppose we have an $n \times n$ matrix $A$ and we want to find  $A^{-1}$ or show that it is not invertible 

We first form an augmented matrix: 
$$ \begin{pmatrix}
A | I_n
\end{pmatrix}
_{n \times 2n}
$$
Then we apply row operations to this matrix to being the left half $A$ to $I_n$. If this works, then we get: $(I_n | A^{-1})$ so $A$ is invertible. It if doesn’t work, then $A$ is not invertible 

Since we can get from $A$ to $I_n$ by applying finitely many row operations, there are elementary $n \times n$ matrices $E_1, E_2, … E_k = B$ s.t. 

$$ E_k(E_2(E_1A)) = I_n \implies (E_k… E_1)A = I_n \implies BA = I_{n}$$
$$ \implies B = A^{-1} $$
#### Why the RHS equals $A^{-1}$

As each row operation can be represented by an elementary matrix $E$, when we do all of them in sequence, we're multiplying their product: 
$$ E_{k} E_{k-1}\dots E_{1}A = I \implies (E_{k}E_{k-1}\dots E_{1}) = A^{-1}$$
But in the augmented matrix form, we've been applying those same exact operations to the identity matrix on the RHS, so the RHS ends up being: 
$$ E_{k}E_{k-1}\dots E_{1}I = A^{-1}$$
And therefore: 
$$ (A|I_{n}) \rightarrow (I_{n}|A^{-1}) $$
#### Example 

Suppose we want to find the inverse of the matrix: 
$$  A = \begin{pmatrix}
2 &1 \\
1& 1 
\end{pmatrix}$$
First we write it in the augmented form: 

$$
\begin{pmatrix}
2 & 1 & | &1 & 0 \\
1 & 1 & | &0 & 1 \\
\end{pmatrix}
$$
We want to scale so that the first pivot is 1, so we have: $R_1 \rightarrow R_1 - R_2$. Remember to perform the same row operations on the RHS as well 
$$
\begin{pmatrix}
1 & 0 & | &1 & -1 \\
1 & 1 & | &0 & 1 \\
\end{pmatrix}
$$
Next, we want to eliminate below the pivot: $R_2 \rightarrow R_2 - R_1$
$$
\begin{pmatrix}
1 & 0 & | &1 & -1 \\
0 & 1 & | &-1 & 2 \\
\end{pmatrix}
$$
Now, as the LHS is $I_2$, this means the RHS is by definition $A^{-1}$. And we can check this by computing: 
$$ AA^{-1} =\begin{pmatrix}
2 &1 \\
1& 1 
\end{pmatrix} 
\begin{pmatrix}
1 &-1 \\
-1& 2 
\end{pmatrix}
= 
\begin{pmatrix}
1 &0 \\
0& 1 
\end{pmatrix}
= I_{2}
$$
## Rank of a Matrix 

[[Tags/Definition\|Definition]] Given a $m \times n$ matrix $A$, the **rank** of $A$ is the number of non-zero rows in **any** REF of $A$ 

The rank essentially measures how many independent rows or columns a matrix has. So for an $n \times n$ matrix, having rank $n$ means that all its columns and rows are linearly dependent. So in this case: 
- No row/column can be written as a combination of others 
- Every pivot position is filled 
- So Gaussian elimination can turn $A$ into $I_n$ so that no zero rows appear 
- This means we can find $A^{-1}$ 

Therefore, if $A$ is an $n \times n$ matrix then $A$ is invertible $\iff$ $rank(A) = n$ 
This is also why if there is a zero row in an RREF form, the inverse of a matrix does not exist 

### Properties of a Rank 

Let $A$ be a $m \times n$ matrix and $B$ be any matrix: 
- $B$ row equivalent to $A$ $\implies$ rank($B$) = rank($A$)
- rank($\lambda A$) = rank($A$), $\lambda \neq 0$ 
- rank($A$) $\leq$ $\min(m,n)$ 
	- Based on the definition of rank, we can never have more than $m$ linearly dependent vectors in $\mathbb{R}^m$ Same with the rows. So as row rank = column rank, the inequality follows. 
- rank($A + B$) $\leq$ rank($A$) + rank($B$) - provided $B$ is $m \times n$ 
- Rank($A + B$) $\leq$ min(rank($A$), rank($B$)) 

# 4.Determinants 

$M_n(\mathbb{R})$ - the set of all $n \times n$ matrices with real entries. We don't start by just saying what the determinant is, but what kind of function it must be. So the axiomatic definitions are given below. Note that these are slightly less formal than what's in the official lecture notes, but that's mostly down to making it easier and more intuitive to understand.  

[[Tags/Definition\|Definition]] 
A function $D: M_n(\mathbb{R}) \to \mathbb{R}$ is a determinant if the following 3 conditions hold: 

#### 1. Linearity in each row  

If we multiply a row by a scalar $\lambda$, then the determinant scales by $\lambda$ 
And if we add the rows, determinants add. So the sum of the determinants is the determinant of the sums 

$$ D (\dots , \lambda r_{i},\dots) = \lambda D(\dots, r_{i}\dots)$$
$$ D(\dots , r_{i} + r_{i} +\dots) = D(\dots, r_{i}, \dots) + D(\dots r^`_{i}, \dots)$$
#### 2. Alternating 

If $A \in M_n(\mathbb{R})$ has two equal rows $\implies$ $D(A) = 0$ 

So if two rows are equal, then the determinant is 0 
Swapping two rows flips the sign of the determinant 

#### 3. Normalisation 

$$ D(I)= 1 , \quad I_{n} = n \times n \text{ identity matrix}$$

Using the axioms above, we can further prove the row operations and their effects on matrices

- Row interchange doesn't change the determinant 
- Swapping rows (row replacement) causes the determinant to be me multiplication by $-1$ as it flips orientation 
- Multiplying a row by a scalar multiplies the determinant by that scalar. 
	- So if $A \rightarrow (R_i \to \lambda R_i) \rightarrow  B \implies D(A) = \frac{1}{\lambda}D(B)$ 

So 
$$ D(B) = \alpha D(A) $$
where $\alpha$ is the type of row operation. 
## Determinants of Upper Triangular Matrices 

[[Tags/Definition\|Definition]] 

An upper triangular matrix is a matrix where all entries below the diagonal are zero: 
$$ A = \begin{pmatrix}
a_{11} & a_{12} & a_{13} & a_{14} & \dots \\
0 & a_{22} & a_{23} & a_{24} & \dots \\
0 & 0 & a_{33}& a_{34} & \dots\\
\vdots & \vdots & \vdots & \ddots  & \vdots\\
0 & 0 & 0 & 0 &  a_{nn}
\end{pmatrix} $$
So if $A$ is an upper triangular matrix, then the determinant of $A$ is the product of the diagonal entries of $A$:  
$$ D(A) = a_{11}a_{22}  a_{33} \dots a_{nn}$$
Intuitively, the matrix $A$ represents a transformation that: 
- Scales the first coordinate by $a_{11}$ 
- Scales second coord by $a_{22}$ 
- Third by $a_{33}$ 
- And it may shear the shape horizontally because of the entries above the diagonal. 

Each diagonal entry $a_{ii}$ is essentially a scaling of one axis direction. So if we started with the identity matrix (which has $D=1$), and just scaled each axis by those number. The volume (which is basically what a determinant is) would be the product of all the diagonal entries. And shearing doesn't change the determinant as it's the same idea as adding a multiple of one row to another. 

A more formal proof can be done by using row operations and transforming the above matrix into $I_n$, and all those transformations involve row replacement options only. 

## Determinant of any square matrix 

Once we have the facts above, we now have an algorithm to compute the determinant of any square matrix: 

To compute $D(A)$: 
- Perform Gaussian elimination to reduce $A$ to an upper triangular form i.e. the REF for a square matrix
- Keep track of how each row operation affects $D$ 
- Compute the determinant of the upper triangular matrix 

Notation wise, determinant of $A$ = $|A| = \det A$ 

### Proof for a $2 \times 2$ matrix 

For 
$$ A = \begin{pmatrix}
a & b \\ 
c & d 
\end{pmatrix}$$
$$\det(A) = ad - bc $$
Geometrically speaking, in $\mathbb{R}^2$, the two column vectors of $A$ span a parallelogram. And the area of that  = $|ad-bc|$ 
- The sign of $ad-bc$ tells us if the orientation is preserved or flipped. If the parallelogram collapses to a line (area = 0), then then two vectors are linearly dependent, i.e. the matrix is not invertible. 
- That's why $A^{-1} \iff \det(A) \neq 0$ 
- In the similar way, the rank tells us what the shape "collapses" to in higher dimensions. 

Now, for the more formal proof, we can compute $\det(A)$ by performing row operations until we make $A$ upper triangular, and then take the product of the diagonal entries 

We can do the row operations $R_2 \to R_2 - \frac{c}{a} R_1$ which gives us: 
$$ B = \begin{pmatrix}
a & b \\ 
0 & d-\frac{c}{a}
\end{pmatrix} $$
From the property of determinants, the row replacement does not change the determinant, so $\det(B) = \det(A)$. Now as $B$ is upper triangular, we can calculate the determinant by: 
$$ \det(B) = a\left( d - \frac{c}{a}b \right) = ad-bc$$
Therefore, $\det(A) = ad-bc$ 


**The determinant of a matrix with integer entries is always an integer** 

### Existence and Uniqueness 

$\forall n \in \mathbb{N}, \space \exists$ **unique** determinant $D : M_n (\mathbb{R}) \to \mathbb{R}$ satisfying the axiomatic definitions of determinants 

This will be proved in Linear Algebra II by giving a different definition of determinant. So the lesson is to never trust anything. 

## Determinants and Invertibility 

$$ \text{ An $n \times n$ matrix is invertible $\iff$ $\det(A) \neq 0$}$$
### Proof 

Starting with the $\implies$ side: 

If $A$ is invertible, then $\exists A^{-1}$ s.t. $AA^{-1} = I_n$ 

Now we can take the determinant of both sides 
$$ \det(AA^{-1}) = \det(I_{n}) \implies \det(A) \det(A^{-1}) = 1 \implies \det(A) = \frac{1}{\det(A^{-1})}$$
This means that $\det(A) \neq 0$ as $1/0$ is not defined 

Now for $\impliedby$ 
For a bit of intuition, recall that the determinant is geometrically the scaling factor of volume when $A$ acts as a linear transformation. So if $\det(A) = 0$, then the volume collapses to a lower dimension, and that transformation is not reversible. 

Now for the algebraic proof. We know that when we apply Gaussian elimination to turn $A$ into an upper triangular matrix ($U$): 
$$ A = E_{k}\dots E_{2}E_{1}U$$
Each $E_i$ is an elementary matrix which is invertible. So we have that: 
$$ \det(A) = (\det(E_{k}).. \det(E_{1})) \det(U)$$
Now, if $\det(A) \neq 0 \implies \det(U) \neq 0$ 
But $\det(U)$ is the product of diagonal entries, so none of them can be zero. This means that all pivot positions in Gaussian elimination are non-zero, which means we can reduce $A$ all the way down to $I_n$. Hence $A$ is invertible 

There is another proof by contrapositive, given in the lectures notes. 
So if we can prove that $A$ is not invertible, then $\det(A) = 0$, that will be same as proving the original statement 

So if $A$ is not invertible, it means rank $A < n$. This means that for any REF form $B$ of $A$, $B$ has a row a zeroes. But $A$ can be reduced to this REF form via a finite sequence of row operations, so $\det(B) = \beta \cdot \det(A)$ for some $\beta \neq 0$. 
$$ \det(A) = \frac{1}{\beta} \det(B) = 0 \implies \text{ B has a zero row}$$
And if a matrix has a zero row, the determinant will be $0$ as the it's the product of diagonals in a upper triangular matrix.  

## Determinant using Cofactors 

Now that we know how to calculate the determinant of a $2 \times2$ matrix, we want to a formula that still captures that same alternating and linear property. And the cofactor expansion can be thought of as a recursive way to do this, it breaks down a big determinant into small ones (minors)

So if $A$ is an $n \times n$ matrix, then $\det(A)$ is defined in terms of $(n-1) \times (n-1)$ determinants. 

For some definitions, consider an $n \times n$ matrix $A = (a_{ij})$
Then: 
- **minor** $M_{ij}$ is the determinant of the smaller matrix we get after deleting the $i$-th row and $j$-th column. 
- **cofactor** $C_{ij}$ adds a sign to the minor: 
 $$ C_{ij} = (-1)^{i+j}M_{ij}$$

So to find the determinant, we pick a row/column, say row 1, then for each element $a_{1j}$ in that row: 
- Delete its row and column from the matrix to get a smaller matrix called the minor 
- Multiply that smaller determinant by $a_{1j}$ 
- Multiply by a sign $(-1)^{1+j}$ that alternates $+ - + - +$ across the row 

So formally, if 
$$ A =  \begin{pmatrix}
a_{11} & a_{12} & a_{13}  \\
a_{21} & a_{22} & a_{23}  \\
a_{31} & a_{32} & a_{33}
\end{pmatrix}
$$
Then


$$ \det(A) = \sum_{i =1}^n a_{1j} c_{1j} + a_{2j} c_{2j} + … + a_{nj} c_{nj} $$
Where 
$$ C_{1j} = (-1)^{1+j} \det (M_{1j})$$
And $M_{1j}$ is the minor obtained by deleting row $1$ and column $j$ 

So the formula for any $n \times n$ matrix $A = (a_{ij})$, expand along the $i$-th row: 
$$ \det(A) = \sum_{j=1}^{n}(-1)^{i+j}a_{ij} \det(M_{ij})$$
The sign pattern comes from one of the determinant axiom which tells us that if we swap two rows, the determinant changes the sign. 

As we're expanding the determinant along a row, we're sort of "isolating" one element $a_{ij}$ and its minor. Intuitively, we're bringing $a_{ij}$ up to position by moving rows/columns around, and to account for that movement, we multiply by $(-1)^{i+j}$ 

This is quite efficient when we have a matrix with lots of zero entries 

## Determinant of a Transpose 

For any square matrix $A$, 
$$ \det(A^T) = \det(A) $$
What this is means transposing a matrix (i.e. flipping rows and columns) of a matrix does not change its determinant 

Intuitively, if we think determinant as the volume scaling factor, then transposing it just changes our point of view, so instead of looking at how $A$ acts on row vectors, you look at how it acts on column vectors. Hence, the volume scaling remains the same. 

The other way to think about is using the fact that the determinant is the product of the diagonals, and when we transpose a square matrix, the diagonals remain the same, hence the determinant is the same. 
## Determinant of a Product 

If $A,B$ are $n \times n$ matrices, then $\det(AB) = \det(A) \det(B)$

Geometrically again, scaling a volume by a factor of $\det(A)$ and scaling it by $\det(B)$ is the same as scaling it by $\det(A)\det(B)$ 

More formally speaking, we can think of every invertible matrix $A$ as a product of elementary matrices: 
$$ A = E_{k} E_{k-1}\dots E_{1}$$
And as each elementary matrix corresponds to a **single** row operation, and because we know how determinant changes under row operations: 
$$ \det(E_{i}A) = \det(E_{i})\det A$$ and since every matrix can be built from the elementary matrices, we have that: 
$$ \det(AB) = \det(A)\det(B)$$
The proof in the notes is bit more detailed and uses the 3 cases of the elementary matrices, but the idea is the same. 

## Powers of a matrix 

$$\det(A^k) = (\det A)^k , \quad\forall k \in \mathbb{Z}$$
$$ \det(A^{-1}) = \frac{1}{\det(A)}$$
The proof is rather trivial, and can be proved by induction if wanted as an exercise to the reader 

## Inverting a Matrix using Cofactors 

This section is skipped as it will not be examined 

# 5.Linear Transformations 

This is where the proper linear algebra starts. A linear transformation is just taking a function from one vector space to another, following a couple of specific rules, namely additivity and scaling. 

[[Tags/Definition\|Definition]] Let $m, n \in \mathbb{N}$, and let $T : \mathbb{R}^n \to \mathbb{R}^n$ be a function. Then $T$ is a **linear transformation** if $\forall \vec{u}, \vec{v} \in \mathbb{R}^n$ and $\forall \lambda \in \mathbb{R}$ we have: 

$$ T(\vec{u} + \vec{v}) = T({\vec{u}}) + T(\vec{v}) $$
$$ T(\lambda \vec{u}) = \lambda T(\vec{u}) = \lambda T(\vec{u})$$

Intuitively, a linear transform never bends, curves, or shifts space, it can only scale, rotate, shear, reflect, etc. So essentially, if the origin doesn't stay fixed, then the transformation is not linear. 

The most important thing is probably this: every linear transformation is a matrix multiplication. 
So if $A$ is an $m \times n$ matrix, then 
$$ T : \mathbb{R}^m \to \mathbb{R}^m \text{ defined by } T(\mathbf{x}) = A\mathbf{x} \ \forall x \in \mathbb{R}^n$$
So every linear transform, is a multiplication by some matrix $A$. So if we know what the transformation does to the basis vectors, we know what it does to every vector in the space. The proof of this is trivial, and is explained in the notes. 

Now that we know that $T : \mathbb{R}^n \to \mathbb{R}^m,$ is a linear transform, then standard basis vectors of $\mathbb{R}^n$ can help us determine the whole transformation. 

Consider the standard basis vectors in $\mathbb{R}^n$ : 
$$e_{i} = (0, \dots 0, 1 , 0, \dots 0) $$
Where the $i$-th entry is the vector entry $1$ 

And we know that any vectors $x$ can be written in terms of the basis vectors: 
$$ \mathbf{x} = x_{1}e_{1} + x_{2} e_{2} + \dots + x_{n} e_{n}$$
So $T$ is linear, then 
$$ T(x) = x_{1}T({e_{1}}) + x_{2} T(e_{1}) + \dots + x_{n}T(e_{n}) = (T(e_{1}) \dots T(e_{n})) \mathbf{x} = A\mathbf{x}$$
Hence just showing the basis vectors, is enough to define the entire transformation. It's like taking the unit square and seeing how it changes under a matrix. 

## Linear Transformation in $\mathbb{R}^2$

Every linear transformation in $\mathbb{R}^2$ is completely determined by: $T(e_1), T(e_2)$, where 
$$ e_{1} = \begin{pmatrix}
1 \\ 
0 
\end{pmatrix} ,\quad  e_{2} = \begin{pmatrix}
0 \\ 
1
\end{pmatrix}$$
So to understand a transformation, we need to think about what it does to $e_1, e_2$

### Rotation about the origin 

Let $T: \mathbb{R}^2 \to \mathbb{R}^2$ be the rotation by $\theta \in [0, 2\pi)$ anti-clockwise about the origin: 

Now think about what happens to $e_1 = (1,0)$, when rotating, it lands at ($\cos\theta, \sin \theta)$ 
And when $e_2 = (0,1)$ is rotated, it lands at $(\cos(\theta + \pi/2), \sin (\theta + \pi/2))$, which simplified is $(-\sin \theta, \cos \theta)$.
Therefore the matrix of rotation is given by: 
$$ A=  \begin{pmatrix}
\cos \theta & -\sin \theta \\
\sin \theta & \cos \theta 
\end{pmatrix} $$
We can check that rotation preserves the area, so the determinant of this matrix is in $\cos^2 \theta + \sin
{ #2}
 \theta = 1$fact 

And therefore the matrix of linear transformation is given by: 
$$ T ( \begin{pmatrix}
x \\ 
y
\end{pmatrix}) = A \begin{pmatrix}
x \\ 
y
\end{pmatrix} = \begin{pmatrix}
\cos \theta x & -\sin \theta y \\
\sin \theta x & \cos \theta y
\end{pmatrix}, \ \forall \begin{pmatrix}
x \\ 
y 
\end{pmatrix} \in \mathbb{R}^2$$

### Reflection in a line through origin 

Note that a reflection keeps points on the line fixes, and flips points perpendicular to the line. There is a diagram in the notes which makes it easy to see why its $2 \theta$, but another way to think about it to consider the basis vectors and how they're changing. 

A reflection through the angle $\theta$ is the same at a rotation by $-\theta$ to align the axis, then reflect across the $x$ axis, and rotate it back by $\theta$ 

The matrix is therefore given by: 
$$T  = \begin{pmatrix}
\cos(2 \theta) & \sin(2 \theta)\\
\sin (2 \theta) & -\cos(2 \theta)
\end{pmatrix} $$
The determinant of this matrix, when calculated, is $-1$ 
### Stretch/shrink 
A scaling just has the effect of multiplying axes. So the matrix here is self-explanatory: 
$$T = \begin{pmatrix}
\lambda & 0 \\ 
0 & \mu 
\end{pmatrix} $$
$T$ stretches/shrinks the plane by $\lambda$ in the direction of the $x$ axis and by $\mu$ in the $y$ axis 

### Shear 