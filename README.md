### Computation of ramification index of modular parametrizations of elliptic curves at cusps.
-----

####1. Rephrasing the problem.

Let $E$ be an elliptic curve over $\mathbb{Q}$. We are


Our code will compute the the "cusp part" of the divisor of the differential $\omega = f(z)dz$.


#####1.2 What's known.

It's known that the ramification index at a big cusp $z$ is one if $z = c/d$ where $N/d$ is prime to 6. Also there is a "multiplicative" relation, where if we factor $d' = N/d$
as $d' =  2^a 3^b \prod p_i^{n_i}$, then
        $$e(d') = e(2^a)e(3^b)$$

Moreover, $e(2^a) > 1$ only if $2a = ord_2(N) \geq 4$; similarly,
$e(3^b) > 1$ only if $2b = ord_3(N) \geq 4$. Since we know in general that
\[
    ord_2(N) \leq 8, ord_3(N) \leq 5.
\]
We have a finite number of possibilities for $a$ and $b$ in order for ramification at cusp. The latter implies $ord_3(N) = 4$.

Finally, $e(2^a)$ is a power of 2,not exceeding 8 and $e(3^b)$ is either 1 or 3. As a consequence,

$$e(d) \text{ is a divisor of 24}.$$

####2. Usage

#####(Note: The file modified-typespace.sage is written based on Professor David Loeffler's code typespace.sage, so the author do not claim any originality).

#####2.1 Examples:

Open a sage worksheet and do

    sage: load('ramification-index')

To test the code, we compute some ramification indices.
First we consider the curve "48a", of which we know
$e(12) = 2$.

    sage: ram_index(EllipticCurve('48a'),2)
    2

A second example where the $ord_2(N) = 6$:


    sage: ram_index(EllipticCurve('64a'),2)
    2

An example where the ramification index is greater than 2.

    sage: ram_index(EllipticCurve('112c'),2)
    4



We try another example, where the denominator is a power of
3.

    sage: ram_index(EllipticCurve('162b'),3)
    3


An example where $2^8$ divides the conductor::

    sage: ram_index(EllipticCurve('768b'),2)
    8

#### How it works.
Upcoming...
