# Vectors

In physics, we distiguish between *scalar* quantities and *vector* quantities:
* Scalars are defined by a single numeric value. Examples include distance, speed, time, temperature, pressure, mass and energy.
* Vectors have associated both a numeric value and a direction. Examples include displacement, velocity, acceleration, force, and momentum.

We depict vectors by arrows whose length is proportional to the magnitude of the quantity in question and whose direction is that of the action of the quantity. In symbols, we will use bold typeface to indicate a vector, such as $\mathbf{v}$, and we will denote a vector from point $A$ to $B$ by $\overrightarrow{AB}$. See figure \@ref(fig:vector).



<div class="figure">
<img src="figures/vector.png" alt="A vector $\mathbf{v}$ between points $A$ and $B$." height="120%" />
<p class="caption">(\#fig:vector)The vector $\mathbf{v} = \overrightarrow{AB}$ is the vector from $A$ to $B$.</p>
</div>


## Vector addition

Geometrically, to add two vectors together we can place the tail of one vector at the head of the other and take the vector that goes from the starting point to the finish point.

<div class="figure">
<img src="figures/vecadd.png" alt="Geometric addition of two vectors $\textbf{v}$ and $\textbf{w}$ by aligning them tail to head." height="120%" />
<p class="caption">(\#fig:label)Addition of two vectors $\textbf{v}$ and $\textbf{w}$ by aligning them tail to head.</p>
</div>

::: {.example #vecadd name="Vector addition"}
A swallow is flying at 40 km/h due north with an easterly wind blowing at a speed of 20 km/h. The swallow's groundspeed can be found by adding the velocity vectors:
\begin{align*}
\mathbf{v} &= 40 \text{ km/h North}\\
\mathbf{w} &= 20 \text{ km/h West}\\
\mathbf{v}+\mathbf{w}&=20\sqrt{5} \text{ km/h North by North West}.
\end{align*}
:::

Alternatively, we can use the parallelogram rule (which amounts to the same thing): we draw a parallelogram with two of the non-parallel sides given by the vectors and take the diagonal as the resultant vector, as in figure \@ref(fig:vecaddpara).


<div class="figure">
<img src="figures/vecaddpara.png" alt="Parallelogram for addition of two vectors $\textbf{v}$ and $\textbf{w}$." height="120%" />
<p class="caption">(\#fig:vecaddpara)Parallelogram for addition of two vectors $\textbf{v}$ and $\textbf{w}$.</p>
</div>

## Scalar multiplication

If we multiply a vector by a positive scalar, we change only the magnitude of the vector and keep its direction. For example, if the sparrow in example \@ref(exmp:vecadd) starts flying twice as fast, we have the velocity vector
$$2\mathbf{v} = 80 \text{ km/h North}.$$
If we multiply by a negative value, the vector now points in the opposite direction:
$$-2\mathbf{v} = 80 \text{ km/h South}.$$

<div class="figure">
<img src="figures/scalarmult.png" alt="Scalar multiplication of a vector $\mathbf{v}$." height="120%" />
<p class="caption">(\#fig:scalarmult)Scalar multiplication of a vector $\mathbf{v}$.</p>
</div>

Finally, if we multiply by $0$, we get the *zero-vector* $\mathbf{0}$, which has magnitude $0$ and no direction:
$$0\mathbf{v}=\mathbf{0}$$.


## Vectors in Cartesian coordinates

We mostly deal with vectors in a Cartesian coordinate system. We then define vectors of length 1 that point out from the origin along the coordinate axes. In three dimensions we label these as $\mathbf{i}$ along the $x$-axis, $\mathbf{j}$ along the $y$-axis and $\mathbf{k}$ along the $z$-axis. In two dimensions we simply drop the $\mathbf{k}$ vector.

We can then write any vector $\overrightarrow{OA}$ from the origin $O$ to a point $A$ as some combination of the these vectors. For example, the vector in the plane from the origin to the point $A=(2,3)$ is given by:
$$\overrightarrow{OA}=2\mathbf{i} + 3\mathbf{j}.$$
We can reconcile this with our geometric understanding of addition of two vectors: we place the vector $2\mathbf{i}$ from the origin to the point $(2,0)$ and then place the tail of the vector $3\mathbf{j}$ at the head of $2\mathbf{i}$ to get to the point $(2,3)$; or, in terms of the parallelogram rule we have a rectangle with sides $2\mathbf{i}$ and $3\mathbf{j}$.

Yet another way to write this vector is as a *column vector*
$$\overrightarrow{OA}=
\begin{pmatrix}
2\\
3
\end{pmatrix}.
$$
Such a representation is called a *coordinate vector*.
More generally, the vector
$$\mathbf{v}=x\mathbf{i}+y\mathbf{j}+z\mathbf{k}$$
can be written as the column
$$\begin{pmatrix}
x\\
y\\
z
\end{pmatrix}.
$$

Now addition and scalar multiplication can be carried out component-wise as follows. If we have
$$\mathbf{v}=x\mathbf{i}+y\mathbf{j}+z\mathbf{k}$$
and
$$\mathbf{w}=x'\mathbf{i}+y'\mathbf{j}+z'\mathbf{k}$$
then
$$\mathbf{v}+\mathbf{w}=(x+x')\mathbf{i}+(y+y')\mathbf{j}+(z+z')\mathbf{k}$$
and with $a$ a scalar,
$$a\mathbf{v}=ax\mathbf{i}+ay\mathbf{j}+az\mathbf{k}.$$

Or, as column vectors with
$$
\mathbf{v} = 
\begin{pmatrix}
x\\
y\\
z
\end{pmatrix},
\qquad
\mathbf{w} = 
\begin{pmatrix}
x'\\
y'\\
z'
\end{pmatrix}
$$
we have
$$\mathbf{v}+\mathbf{w}= \begin{pmatrix}
x+x'\\
y+y'\\
z+z'
\end{pmatrix}.
$$
and
$$
a\mathbf{v} = 
\begin{pmatrix}
ax\\
ay\\
az
\end{pmatrix}.
$$
