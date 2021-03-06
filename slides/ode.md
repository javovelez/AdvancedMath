% Ordinary differential equations
% Nicolás Guarín-Zapata
    email: nguarinz@eafit.edu.co
    github: nicoguaro
% February, 2019



------------------

# Ordinary differential equations

An ordinary differential equation (ODE) is an equation of the form

$$F(z, y, y', y'', \cdots, y^{(n)}) = 0\, ,$$

where $F$ is a function of the independent variable $z$,
dependent variable $y(z)$, and its derivatives.

------------------

# Classification: Number of variables

How many independent variables does the equation have?

\begin{align}
&L\frac{d^2 Q}{dt^2} + R\frac{dQ}{dt} + \frac{1}{C}Q = E  &\text{(ODE)}\\
&\frac{\partial u}{\partial t} =\alpha \frac{\partial^2 u}{\partial x^2}  &\text{(PDE)}\\
&\frac{\partial u}{\partial t} =\frac{\partial^2 u}{\partial r^2} +
    \frac{1}{r} \frac{\partial u}{\partial r} +
    \frac{1}{r^2}\frac{\partial^2 u}{\partial \theta^2}  &\text{(PDE)}
\end{align}

------------------

# Classification: Order

What is the order of the higher derivative?

\begin{align}
&\frac{\partial u}{\partial t} =\alpha \frac{\partial^2 u}{\partial x^2}  &\text{(Second order)}\\
&\frac{d^2 u}{d t^2} = f(t)  &\text{(Second order)}\\
&\frac{d^{(3)} y}{dx^3} + 2 e^x \frac{d^2 y}{d x^2} +
    y\frac{d y}{dx} = x^4  &\text{(Third order)}
\end{align}

------------------

# Classification: Homogeneity

The equation is homogeneous if the right-hand-side of

$$F(z, y, y', y'', \cdots, y^{(n)}) = G(z)\, ,$$

is zero.

------------------

# Classification: Linearity

The equation

$$F(z, y, y', y'', \cdots, y^{(n)}) = 0\, ,$$

is linear if $F$ is a linear function of the variables $y, y', \cdots, y^{(n)}$.

\begin{align}
&\frac{\partial^2 u}{\partial t^2} = e^{-t} \frac{\partial^2 u}{\partial x^2}
  + \sin t  &\text{(Linear)}\\
&\frac{d^2 \theta}{d t^2} = \frac{g}{l}\sin\theta  &\text{(Non-linear)}
\end{align}

------------------

# Classification: Type of coefficients

In the case of linear equations, we analyze the coefficients of the linear
combination. Are these coefficients constant or functions of $x$?

\begin{align}
&a\frac{d^2 u}{d t^2} + b \frac{d u}{d t} + c u  = 0 &\text{(Constant coefficients)}\\
&\frac{d}{dx}\left(x\frac{d w}{dx}\right) = -\omega^2 w  &\text{(Variable coefficients)}
\end{align}


------------------

# Examples: Free fall

<table>
<tr>
<td>
In this case, gravity is the only force acting upon an object. The equation
reads
$$y'' =g = \text{const}$$
</td>
<td>
<video width="640" height="480" autoplay loop>
   <source src="./img/free_fall.mp4" type="video/mp4">
   Your browser does not support the video tag.
</video>
</td>
</tr>
</table>

------------------

# Examples: Parachute falling

<table>
<tr>
<td>
This case is similar to the previous one, but there is air resistance (drag).
The drag force is normally as a constant multiplied by the square of the speed
$$m\frac{d^2 y}{dt^2} = mg - b\left(\frac{dy}{dt}\right)^2$$
</td>
<td>
<video width="640" height="480" autoplay loop>
   <source src="./img/drag_fall.mp4" type="video/mp4">
   Your browser does not support the video tag.
</video>
</td>
</tr>
</table>

------------------

# Examples: Pendulum

<table>
<tr>
<td>
<img src="./img/PenduloTmg.gif"
    width=300
    class="centObj"/>
</td>
<td>
A pendulum is a weight suspended from a pivot that can swing freely. The
equation for a simple pendulum is

$$L\theta'' + g\sin\theta = 0$$
</td>
</tr>
</table>

------------------

# Equations of first order

Equations of first order are of the form

$$\frac{\mathrm{d} y}{\mathrm{d} z} = f(z, y)\, .$$

For an arbitrary function $f$ there is not method for solving this equation
in terms of elementary functions.

------------------

# Linear equations of first order

They are of the form

$$a_0(z) y' + a_1(z) y = f(z)\, .$$

We are assuming that $a_0(z)$, $a_1(z)$, and $f(z)$ are continuous.

------------------

# Linear equations of first order: homogeneous case

We can write it as

$$\frac{\mathrm{d}} {\mathrm{d}z}\ln y + \frac{a_1(z)}{a_0(z)} = 0\, ,$$

after integration

$$y = y_0 \exp\left[-\int\limits_{z_0}^z \frac{a_1(t)}{a_0(t)}\mathrm{d}t\right]\, .$$

------------------

# Linear equations of first order: inhomogeneous case

To solve the equation

$$y' + \frac{a_1(z)}{a_0(z)} y = \frac{f(z)}{a_0(z)}\, ,$$

with $y(0)=y_0$, we use the adjoint equation

$$x' - \frac{a_1(z)}{a_0(z)} x = 0\, ,$$

with $x(0) = 1$.

------------------

# Linear equations of first order: inhomogeneous case

And we solve the differential equation

$$(xy)' = xy' + x' y = x\frac{f(z)}{a_0(z)}\, ,$$

and, after integration

$$y = \frac{y_0}{x} + \frac{1}{x}\int\limits_{0}^{z}\frac{x f(t)}{a_0(t)}\mathrm{d}t\, .$$

------------------

# Systems of differential equations

Sometimes we have more than one differential equations. For example,

$$
\begin{align}
&F_1(z, y_1, y_1', y_1'', y_2, y_2') = 0\, ,\\
&F_2(z, y_1, y_1', y_2, y_2', y_2'', y_2''') = 0\, .
\end{align}
$$


------------------

# Systems of differential equations

Using the new variables

$$
\begin{align}
&x_1 = y_1\, ,  & x_4 = y_2'\, ,\\
&x_2 = y_1'\, , & x_5 = y_2''\, ,\\
&x_3 = y_2\, ,  &
\end{align}
$$

we can rewrite the following system

$$
\begin{align}
&x_1' = G_1(z, x_1, x_2, x_3, x_4) = x_2\, ,\\
&x_2' = G_2(z, x_1, x_2, x_3, x_4)\, ,\\
&x_3' = G_3(z, x_1, x_2, x_3, x_4) = x_4\, ,\\
&x_4' = G_4(z, x_1, x_2, x_3, x_4) = x_5\, ,\\
&x_5' = G_5(z, x_1, x_2, x_3, x_4)\, .\\
\end{align}
$$


------------------

# Power series solutions

Consider the second-order linear differential equation

$$a_0(z)f''(z)+a_1(z)f'(z)+a_2(z)f(z)=0\, ,$$

where $a_0$ is nonzero for all $z$, and $a_1/a_0$ and $a_2/a_0$ are analytic
functions.

The power series method calls for the construction of a power series solution
$$f=\sum_{k=0}^\infty A_kz^k\, ,$$

to find the form of the coefficients $A_k$.

------------------

# Power series solutions: Example 1

Consider the equation

$$y' = y\, .$$

Assuming $y=\sum_{k=0}^\infty A_k z^k$, leads to

$$\sum_{k=1}^\infty[A_{k-1} - k A_k] z^k = 0\, ,$$

or

$$A_k = \frac{A_{k-1}}{k}\, .$$

------------------

# Power series solutions: Example 2

Consider the (not so simple) equation

$$y'' - z y = 0\, .$$

Assuming $y=\sum_{k=0}^\infty A_k z^k$, leads to

$$2A_2 + \sum_{k=1}^\infty[(k + 2)(k + 1)A_{k+2} - A_{k-1}] z^k = 0\, .$$

------------------

# Power series solutions: Example 2

We obtain the general solution

\begin{align}
y(z) =&
C_0\left[1 +
\sum_{k=1}^{\infty} \frac{z^{3k}}{(2\cdot 3) (5\cdot 6) \cdots ((3k-1) \cdot (3k))}\right]\\
   &+ C_1\left[z +
\sum_{k=1}^{\infty} \frac{z^{3k+1}}{(3\cdot 4) (6\cdot 7) \cdots ((3k) \cdot (3k+1))}\right]
\end{align}

------------------

# Power series solutions: Example 2


<table>
<tr>
<td>
These series represent a group of _special functions_ named Airy functions

$$y(z) = \mathrm{Ai}(z) + \mathrm{Bi}(z)\, ,$$

due to the British astronomer George Biddel Airy.

They appear in the solution of Scrödinger equation for a particle
confined within a triangular potential. They are also important
in microscopy and astronomy.
</td>
<td>
<img src="./img/airy_functions.svg"
    width=700
    class="centObj"/>
</td>
</tr>
</table>

------------------

# Power series solutions: A nonlinear example

The equation $x' = 1 + x^2$, with initial condition $x(0) = 0$, has the
solution $x = \tan(t)$. We could use the power series method, assuming
$x = \sum_{k=0}^\infty A_k t^k$, to obtain

$$\sum_{k=0}^{\infty} (k + 1) A_{k+1} t^k =
1 + \left(\sum_{k=0}^{\infty} A_k t^k\right)^2 =
1 + A_0^2 + \sum_{k=1}^\infty\left[\sum_{j=0}^{k} A_j A_{k-j}\right]t^k$$

and the coefficients are

\begin{align}
A_0 &= 0\\
A_1 &= 1 + A_0^2\\
A_{k + 1} &= \frac{1}{k + 1}\sum_{j=0}^{k} A_{k} A_{j - k}\quad \forall k\in \mathbb{N}
\end{align}

------------------

# Frobenius method

This method gives as a way to find infinite series solutions for the
differential equation

$$z^2 u'' + p(z) z u'' + q(z) u = 0\, ,$$

in the vinicinity of the regular singular point $z=0$. We could divide by
$z^2$ to obtain

$$u'' + \frac{p(z)}{z} u' + \frac{q(z)}{z^2} u = 0\, .$$


------------------

# Frobenius method

We are looking for a solution of the form

$$u(z) = \sum_{k=0}^\infty A_k z^{k + r}\quad A_0\neq 0, r\in \mathbb{R}\, ,$$

that leads us to the equation

\begin{align}
  0 =&[r (r - 1) + p(z) + q(z)]A_0 z^r \\
  &+ \sum_{k=1}^{\infty} [(k + r - 1)(k + r) + p(z)(k + r) + q(z)]A_k z^{k + r}
\end{align}

------------------

# Frobenius method

The expression

$$I(r) \equiv r(r - 1) + p(0)r + q(0)$$

is called the inditial equation, and its roots give us the values for $r$.

Depending on the values for the roots, we have different ways to obtain
two linearly independent solutions.


------------------

# Frobenius method: Case 1


The roots do not differ by an integer

\begin{align}
y_1 &= \sum_{k=0}^\infty A_k z^{k + r_1}\quad A_0\neq 0\\
y_2 &= \sum_{k=0}^\infty A_k z^{k + r_2}\quad A_0\neq 0
\end{align}

------------------

# Frobenius method: Case 2


The roots do differ by an integer

\begin{align}
y_1 &= \sum_{k=0}^\infty A_k z^{k + r_1}\quad A_0\neq 0\\
y_2 &= C y_1 \ln(z) + \sum_{k=0}^\infty A_k z^{k + r_2}\quad A_0\neq 0
\end{align}

where $C$ is a constant that could be zero.

------------------

# Frobenius method: Case 3


The roots are the same

\begin{align}
y_1 &= \sum_{k=0}^\infty A_k z^{k + r_1}\quad A_0\neq 0\\
y_2 &= y_1 \ln(z) + \sum_{k=0}^\infty A_k z^{k + r_2}\quad A_0\neq 0
\end{align}

------------------

# Bessel equation

The Bessel equation is of the form

$$z^2 y'' + z y' + (z^2 - \nu^2) y = 0\, .$$

And it appears frequently when solving problems in cylindrical or spherical
coordinates. Particularly, when solving the temperature distribution of a
circular plate or the vibration or a membrane.


------------------

# Bessel equation: Sketch of solution

After pluging our infinite series we obtain

$$A_0 (r^2 - \nu^2) z^r + z^r\sum_{k=1}^\infty A_k [(n + r)^2 - \nu^2]z^n +
z^r \sum_{k=0}^\infty A_k z^{n + 2} = 0 $$

And the indicial equation

$$r^2 - \nu^2 = 0$$

has as solutions $r_1 = \nu$, $r_2 = -\nu$.

------------------

# Bessel equation: Sketch of solution


If we solve the recurrence relations for $r_1 =\nu$, we end up with


$$A_{2k} = -\frac{A_{2k - 2}}{2^2 n (n + \nu)}$$

and the solution renders

$$y = A_0 \sum_{n=0}^\infty \frac{(-1)^n}{2^n n! (1 +\nu)(2 + \nu)\cdots(n + \nu)}
\left(\frac{z}{2}\right)^{2n + \nu}\, .$$


------------------

# Bessel equation: Sketch of solution

We could rewrite this _prettier_ using the Gamma function

$$y = A_0 \sum_{n=0}^\infty \frac{(-1)^n}{n! \Gamma(1 + \nu + n)}
\left(\frac{z}{2}\right)^{2n + \nu}\, ,$$

or simply

$$y = A_0 \mathrm{J}_\nu(z)\, .$$

------------------

# Bessel functions of the first kind


<table>
<tr>
<td>
They appear as the solution of Bessel equation for integer or positive $\nu$.

For non-integer $\nu$, the functions $\mathrm{J}_\nu(z)$ and
$\mathrm{J}_{-\nu}(z)$ are linearly independent.
</td>
<td>
<img src="./img/bessel_functions.svg"
    width=700
    class="centObj"/>
</td>
</tr>
</table>



------------------

# Gamma function

<table>
<tr>
<td>
The gamma function is an extension of the factorial

$$\Gamma(n) = (n - 10)!\, .$$

The Gamma function is defined for all complex numbers except for non-positive
integers. For complex numbers with a positive real part, it is defined via a
convergent improper integral:
$$\Gamma(z) = \int_{0}^{\infty} t^{z-1} e^{-t} \mathrm{d}t\, .$$
</td>
<td>
<img src="./img/gamma_function.svg"
    width=700
    class="centObj"/>
</td>
</tr>
</table>

------------------

# References

- H. Hochstadt. Differential equations: a modern approach.
  Courier Dover Publications, 1975.

- Erwin Kreyszig. Advanced engineering mathematics. John Wiley & Sons, 2010.

- Dennis G. Zill. Ecuaciones diferenciales: con aplicaciones demodelado.
  Iternational Thomson Editores, 1997.

- Ruryk, 2011. Oscilatting pendulum. Retrieved from:
  https://commons.wikimedia.org/wiki/File:PenduloTmg.gif
