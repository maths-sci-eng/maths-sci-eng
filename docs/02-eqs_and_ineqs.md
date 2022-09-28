# Equations and Inequalities

## Equations

An equation indicates the *equality* of two mathematical expressions: what is on the left of the $=$ sign is the same as what is on the right of the $=$ sign. When manipulating equations, we must perform the same operation to each side in order to maintain equality -- think about a traditional mechanical balance scale, where if we were to change the mass on one side of the balance we would need to do the same to the other side in order to maintain balance. We will use the abreviations l.h.s. for left-hand-side and r.h.s. for right-hand-side. There are a few subtly different types of equations; the main two are *formulas* and *conditional equations*.

### Formulas

Equations are often regarded as *formulas*, which can be used to calculate the value of a mathematical or physical quantity in terms of other known quantities. In this case, we write a single *dependent* variable on the left hand side and the right hand side will contain *independent* variables and constants. The value of the dependent variable *depends* on the values of the independent variables and is obtained by evaluating the right hand side when the values of the independent variables are known. For example, the formula for the area $A$ of a circle is

$$A=\pi r^2$$

where the independent variable $r$ is the radius of the cirle and $\pi$ is the mathematical constant $3.141...$. By plugging in a particular value for $r$ we then obtain a value for the area $A$.  We often want to re-arrange equations to make a different variable the dependent variable, or *subject*, of the formula, i.e. to place it alone on the left hand-side. Re-arranging formulae is also known as *transposition*. For example, if we knew the area of a cirlce and wanted to calculate the corresponding radius, we can re-arrange the equation to make $r$ the subject:

$$r=\sqrt{\frac{A}{\pi}}.$$

In obtaining this, we carry out the "opposite" of the operations on the right hand side to both sides of the equation. These opposites are:

* addition and subtraction;
* multiplication and division;
* powers and roots.

Let's see this step by step in our example. We start with 

$$A=\pi r^2.$$

Then, divide both sides by $\pi$

$$\frac{A}{\pi}=\frac{\pi}{\pi}r^2=r^2$$

so that $r^2$ is no longer multiplied by $\pi$. Now, to get from $r^2$ to $r$ we need to take the square root of both sides

$$\sqrt{\frac{A}{\pi}}=\sqrt{r^2}=r$$

and finally, we put the subject on the left hand side (since we read from left to right it is simply convention to do this, but mathematically it makes no difference since it is still an equality).

### Conditional equations

Another type of equation is a *conditional* equation. These may not hold true for all values of the variables and we will want to find the values for which equality is true. For example,
$$5x+4=19$$
is only true when $x=3$. We can solve this equation by making $x$ the subject:

subract $4$ from both sides

$$5x=15$$

divide both sides by $5$

$$x=3.$$

Note that an equation may have more than one solution, or perhaps no solutions. For example,

$$x^2=4$$

has two possible solutions, either $x=2$ or $x=-2$. On the other hand, the equation

$$x+2=x+3$$

has no solutions. To see this, subtract $x+2$ from both sides and we obtain

$$0=1$$

which is false, so no value of $x$ can give us equality.

### Quadratic equations {#quad-eqs}

A particularly common form of equations that arise in science and engineering are *quadratic* equations. These are equations of the form

$$ax^2+bx+c=0$$

where $a$, $b$ and $c$ are constants and we wish to find the values of $x$ satisfying this equation. We explore three different methods below.

#### Factorisation by inspection

First consider a quadratic where $a=1$, that is

$$x^2+bx+c=0.$$

If we can write a quadratic equation as a product of two simple linear factors in the form^[In fact, any quadratic can be factorised as a product of two linear factors, but we may need complex numbers to do this; more on this in section \@ref(complex).]:

$$x^2+bx+c = (x+\alpha)(x+\beta)$$

then $x=-\alpha$ and $x=-\beta$ are solutions to $ax^2+bx+c=0$, since for $x=-\alpha$

$$(-\alpha+\alpha)(-\alpha+\beta)=0(-\alpha+\beta)=0$$

and similarly for $x=-\beta$. Furthermore, these will be the only two solutions: it is possible there are two different solutions $\alpha\neq\beta$, one "repeated" solution where $\alpha=\beta$ so that the quadratic factorises as $(x+\alpha)(x+\alpha)=(x+\alpha)^2$, or there may be no solutions^[That is, no solutions for which $\alpha$ and $\beta$ are real numbers, but there will instead be complex number solutions.]. In many cases it is easy to spot the values of $\alpha$ and $\beta$. To see this, let's work backwards and expand the brackets:

$$(x+\alpha)(x+\beta)=x^2+\beta x +\alpha x +\alpha\beta = x^2 + (\alpha + \beta)x + \alpha\beta$$

so we just need to find the values of $\alpha$ and $\beta$ that sum to $b$ and multiply together to give $c$.

::: {.example #factorise}
If we have
$$x^2+5x+6=0$$
we are looking for two numbers that sum to make $5$ and multiply to make $6$, so the answer is clearly $x=2$ and $x=3$, giving the factorisation
$$x^2+5x+6=(x+2)(x+3).$$
:::

If we have a more general quadratic where $a\neq1$, then we could start by taking out a factor of $a$
$$ax^2+bx+c=a\left(x^2+\frac{b}{a}x+\frac{c}{a}\right)=0$$
and then dividing both sides by $a$
$$x^2+\frac{b}{a}x+\frac{c}{a}=0$$
The values of $x$ satisfying this new equation will be the same as those for the original, so we can now use the above method to find the solutions. However, sometimes we not only want the solution, but also want to know how to factorise the quadratic. In this case we shall have to keep the factor of $a$. To factorise we just need to find the values of the coefficients in the factorisation that will give the answer we need when we expand the brackets.

::: {.example #factorise2}
Solve $4x^2 + 8x + 3 = 0$ by factorising.

We need the $x$ terms to multiply together to make $4x^2$, so we could have either
$$(4x + \star)(x + \star)$$
or
$$(2x + \star)(2x + \star)$$
and we need the constant terms to multiply together to make $3$, so we could have either
$$(\star + 3)(\star + 1)$$
or
$$(\star - 3)(\star - 1).$$
The sum of the products of the outer terms and inner terms needs to be $8x$ and the only way this is possible is with
$$(2x+3)(2x+1).$$

The solutions then come from solving for each factor being $0$, giving
$$x=-\frac{3}{2}\quad\text{ or }\quad x= -\frac{1}{2}$$
:::

Not all quadratics will factorise "nicely", that is to say, where the coefficients in the linear factors will be integers. We can first test if the quadratic will factorise with integer coefficients by computing the quantity

$$\Delta = b^2 - 4ac$$

which is known as the *discriminant* of a quadratic: if this number is a perfect square, then the linear factors will have integer coefficients; if it is not a perfect square, the coefficients will not be integers.

In the case where the coefficients are not integers it can be difficult to determine the coefficients by inspection and the following two methods can be applied instead.

#### Completing the square

In this method, we first rewrite a quadratic equation
$$ax^2+bx+c=0$$
into the form
$$a(x-h)^2+k=0$$
that is, a squared term plus a constant, hence the name "completing the square".

We then solve by rearranging and taking sqaure roots
\begin{align*}
(x-h)^2+k&=0\\
(x-h)^2&=-k\\
x-h&=\pm\sqrt{-k}\\
x&=h\pm\sqrt{-k}
\end{align*}
where $\pm$ means there is one solution coming from taking the $+$ option and the other from taking the $-$ option.

We just need to find $h$ and $k$. They are given by
$$h=-\frac{b}{2a},\quad k=c-\frac{b^2}{4a}.$$

It is not necessary to remember these formulae, we can instead figure out the coefficients as we go along.

::: {.example #completesqr name="Completing the Square"}
Consider the quadratic equation
$$2x^2+12x-26=0.$$
We first take out the factor $a=2$
$$2x^2+12x-26=2(x^2+6x-13)$$
Next we can make a square term that agrees with the first two terms by taking half the $x$ coefficient (i.e. $6\div2=3$):
$$(x+3)^2=x^2+6x+9.$$

This differs from the required result in the constant term by
$$-13-9=-22$$
and so we need to "complete the square" by adding $-22$, to obtain
$$2x^2+6x+13=2[(x+3)^2-22]=2(x+3)^2-44.$$

The solutions are then
\begin{align*}
2(x+3)^2-44&=0\\
2(x+3)^2&=44\\
(x+3)^2&=22\\
x&=-3\pm\sqrt{22}.
\end{align*}
:::


#### The quadratic formula

Sometimes it is difficult to find the solutions using the above methods and so thankfully we have a forumula for finding them (or to determine if there are no real number solutions).

::: {.theorem #quadform name="Quadratic Formula"}
The solutions to the quadratic equation
$$ax^2+bx+c=0$$
are given by
$$x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}.$$

If the quantity $\Delta = b^2-4ac$, known as the *discriminant*, is such that $\Delta = 0$ then there will be one repeated solution; if $\Delta$ is negative, then there are no real number solutions (since we cannot take the square root of a negative number).
:::

::: {.exercise #quadform}
Derive the quadratic formula. Hint: use the method of "completing the square" on a general quadratic equation.
:::

### Simultaneous equations

Sometimes a problem will be formulated in terms of multiple equations with multiple, shared variables. The set of equations usually represent constraints between the variables and we need to determine which values of the variables are valid solutions, i.e. which values satisfy all of the equations *simultaneously* -- hence such sets of equations are known as *simultaneous equations*. Sometimes we can solve simultaneous equations by rearranging one equation to set one of the variables as the subject and then substitute this into another equation in order to eliminate one of the variables.

::: {.example #simul-lin}
Given the following two simultaneous equations in the variables $x$ and $y$
\begin{align*}
3x+2y&=5\\
x-4y&=1
\end{align*}
we could rearrange the second equation to make $x$ the subject
$$x=1+4y$$
and then substitute this back in for $x$ in the first equation
$$3(1+4y)+2y=5$$
and then solve for $y$
\begin{align*}
3(1+4y)+2y&=5\\
3+12y+2y&=5\\
14y&=2\\
y&=\frac{1}{7}.
\end{align*}
Now that we have the value for $y$ we can substitute this back into either equation to find $x$. Since we already rearranged the second equation to make $x$ the subject, we might as well use that one:
$$x=1+4y=1+\frac{4}{7}=\frac{11}{7}.$$
Hence the solution is
$$x=\frac{11}{7},\quad y=\frac{1}{7}.$$
:::

The above example shows a particular type of simultaneous equations called *linear* simultaneous equations (if we were to plot a graph of each of the equations we would see that they form straight lines, hence the term *linear*). We shall look at a systematic way to deal with linear simultaneous equations in section \@ref(linear).

::: {.example #simul-nonlin}
Given the following two simultaneous equations in the variables $x$ and $y$
\begin{align*}
2x+y&=7\\
x^2-xy&=6
\end{align*}
it will be easiest to rearrange the first equation for $y$, to get
$$y=7-2x$$
and then substituting this into the second equation
\begin{align*}
x^2-x(7-2x)&=6\\
3x^2-7x-6&=0\\
(3x+2)(x-3)&=0\\
\end{align*}
so the factorisation tells us
$$x=-\frac{2}{3},\text{ or } x = 3.$$
Now substiting these two possibilities back into the first equation gives
\begin{align*}
2(-\frac{2}{3})+y&=7\\
y&=\frac{25}{3}
\end{align*}
and
\begin{align*}
2(3)+y&=7\\
y&=1.
\end{align*}
To summarise, the solutions are:
$$x = -\frac{2}{3},\quad y = \frac{25}{3}$$
and
$$x=3,\quad y=1.$$
:::

The examples presented above are relatively simple, and in some real-world scenarios equations might be very complicated, or even impossible, to solve by hand. In these cases we need to turn to computational techniques. We'll look at some computational techniques in section \@ref(numerics).


## Inequalities

We are familiar with the symbols $<, \leq, >$ and $\geq$, (less than, less than or equal to, greater than and greater than or equal to) which are used to define inequalities.

::: {.example #ineqs}
$$x<5$$ denotes all numbers that are strictly less that $5$ (so not including $5$ itself).
$$-1< x \leq 1$$ denotes all numbers that are strictly greater than $-1$ but less that or equal to $1$ (so $x=1$ is a possibility).
:::

When solving inequalities (i.e. finding values of $x$ which satisfy the expression) we need to be a bit more careful with their manipulation than with equalities. If we perform the same operation to both sides in an equality then the equality still holds true, but this is not the case in general for inequalities -- in particular we need to be careful with multiplication by negative numbers which "flips" the inequality.

Let $a,u,v,x,y,z$ be real numbers, then some basic relations that hold true are:

* if $x>y$ and $y>z$, then $x>z$;
* if $x>y$, then $x+z>y+z$ and $x-z>y-z$;
* if $x>y$ and $u>v$, then $x+u>y+v$;
* if $x>y$, then $ax>ay$ if $a>0$, and $ax < ay$ if $a<0$;
* if $x>y$, then $\dfrac{x}{a}>\dfrac{y}{a}$ if $a>0$, and $\dfrac{x}{a}<\dfrac{y}{a}$ if $a<0$;
* if $x>y>0$ and $u>v>0$, then $xu>yv$ and $\dfrac{x}{v}>\dfrac{y}{u}$;
* if $x>y>0$, then $\dfrac{1}{x}<\dfrac{1}{y}$.

It should not be necessary to memorise all of these, it just requires a little thought when manipulating inequalities: the important ones to be careful with are multiplying or dividing by negative values.

Assume we are comparing two expressions $P$ and $Q$ that depend on the variable $x$ and need to find, for example, the values of $x$ for which $P>Q$. Let us take a look at a range of examples to see how to solve these types of problems.

::: {.example #solvineqs}
We wish to find all values of $x$ satisfying the following inequalities.

1. $2x+6<18.$

    Here we can easily re-arrange the inequality (subtract $6$ from each side and divide by the positive number $2$ -- which preserves the direction of the inequality) to obtain
    $$x<6.$$

1. $x^2-7x+12>0$

    Factorise the l.h.s. to give $(x-3)(x-4)>0$, so to be positive the factors on the left need to be either both positive or both negative, i.e.:

    a. $(x-3)>0$ and $(x-4)>0$, so we must have both $x>4$ and $x>3$, which means that we must take $x>4$.

    a. $(x-3)<0$ and $(x-4)<0$, so we require both $x<3$ and $x<4$, which means we must take $x<3$.
    
    Since either situation a or b satisfies the inequality the solution is $x<3$ or $x>4$.

1. $\left|10-3x\right|\leq 8$, where $|\cdot|$ denotes the absolute value. We must have both:
    a.
        \begin{align*}
        10-3x&\leq 8\\
        -3x&\leq-2\\
        x&\geq \frac{2}{3}
        \end{align*}
        
        i.e. the interval $x\geq\dfrac{2}{3}.$
        And,

	a. $-(10-3x)\leq 8$, leading to $x\leq 6$.

    Hence $\dfrac{2}{3}\leq x \leq 6$.

1. $\dfrac{1}{x-3}>\dfrac{1}{x-2}$
   
    Let's first do this the wrong way to illustrate a point. Let's multiply both sides by $(x-2)$ to obtain
    \begin{gather*}
    \frac{x-2}{x-3}>1\\
    \frac{x-2}{x-3}-1>0\\
    \frac{(x-2)-(x-3)}{x-3}=\frac{1}{x-3}>0
    \end{gather*}
    giving the solution $x>3$.

    We can check the solution graphically by plotting the l.h.s. and r.h.s. and seeing where the l.h.s. is greater than the r.h.s.

    <div class="figure">
    <iframe src="https://www.desmos.com/calculator/ld9jyh4z3y?embed" width="672" height="400px" data-external="1"></iframe>
    <p class="caption">(\#fig:ineq)A plot of the inequality $\frac{1}{x-3}>\frac{1}{x-2}$: the solid red line is the l.h.s and the dashed blue line is the r.h.s.. We are interested in finding the values of $x$ where the red line is above the blue line (the red-shaded region). [[Open graph in browser.]](https://www.desmos.com/calculator/ld9jyh4z3y)</p>
    </div>

    It would appear that something has gone wrong! There is a second interval $x<2$ where the inequality holds true. The problem is that we multiplied by the factor $(x-2)$ forgetting the fact that $x$ is a variable, so this factor could be positive or negative depending on the value of $x$ and hence can flip the inequality. We could still perform this multiplication so long as we keep track of the two possible cases when $(x-2)$ is positive or negative. However, a safer strategy is to first subtract the r.h.s. from the l.h.s., then factorise as much as possible:
    
    $$\frac{1}{x-3}-\frac{1}{x-2}=\frac{(x-2)-(x-3)}{(x-3)(x-2)}=\frac{1}{(x-3)(x-2)}>0.$$

    Hence for the denominator to be positive we must have either $x>3$ and $x>2$, or $x<3$ and $x<2$. Together these yield the solution $x<2$ or $x>3$.
:::

The general strategy for finding $P>Q$ (or similar) is therefore: (1) Consider $P-Q$ and factorise as much as possible; (2) Determine the sign of each factor of $P-Q$ for varying $x$; (3) Determine when $P-Q>0$ (and hence when $P>Q$).


## Common mistakes!

We finish this section with some common algebraic errors to watch out for! Invent your own examples to convince yourself that these things are true.

**Fractions:** $\frac{a}{b+c}\neq \frac{a}{b}+\frac{a}{c}$ and $\frac{a+b}{c+b}\neq\frac{a}{c}$ (can't "cancel" the $b$'s.).

**Inequalities:** $ab>c$ does not imply that $a>\frac{c}{b}$ (what happens if $b$ is negative?).

**Powers:** $(a+b)^2\neq a^2+b^2$.

**Roots:** $\sqrt{a+b}\neq \sqrt{a}+\sqrt{b}$.
