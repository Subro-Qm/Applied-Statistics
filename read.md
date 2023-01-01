## PR**ODUCT MEASURES:**

 The Cartesian product of two sets $X$ and $Y$ is the set of all ordered pairs $(x,y)$ where $x$ is an element of $X$ and $y$ is an element of $Y$. It is often denoted by $X \times Y$.

For example, the 2-dimensional plane $\mathbb{R}^{2}$ can be thought of as the Cartesian product of the real numbers $\mathbb{R}$ with itself, and is therefore equal to $\mathbb{R} \times \mathbb{R}$. Similarly, the 3-dimensional space $\mathbb{R}^{3}$ is equal to $\mathbb{R} \times \mathbb{R} \times \mathbb{R}$.

A rectangle in the context of measure theory is a subset of the Cartesian product of two sets $X$ and $Y$ that can be expressed as the product of two measurable subsets of $X$ and $Y$, respectively. In other words, a rectangle is a subset of the form $U \times V$, where $U \subseteq X$ and $V \subseteq Y$ are measurable sets. This concept is often used in the study of measures and integration on product spaces.

For example, a usual rectangle in the 2-dimensional plane is a set of the form $[a,b] \times [c,d]$, where $[a,b]$ and $[c,d]$ are intervals on the real line. A pair of head/tail observations, such as ${ \text{head} } \times { \text{tail} }$, is also a rectangle.


The product measure of two measures $\mu_X$ on $X$ and $\mu_Y$ on $Y$ is a measure defined on the Cartesian product space $X \times Y$. It is defined by the formula $\mu_X \otimes \mu_Y(U \times V) = \mu_X(U) \mu_Y(V)$, where $U \subseteq X$ and $V \subseteq Y$ are measurable sets.

The product measure has the property that its density is equal to the product of the densities of the original measures. This means that if we have two measures with densities $f_X(x)$ and $f_Y(y)$, respectively, then the density of the product measure will be equal to $f_X(x) f_Y(y)$.

For example, in the 2-dimensional plane, the area of a rectangle $[a,b] \times [c,d]$ is equal to the product of its length and width, which are given by $(b-a)$ and $(d-c)$, respectively. This can be expressed as $(b-a)(d-c) = \operatorname{length}([a,b]) \otimes \operatorname{length}([c,d])$. Similarly, in 3-dimensional space, the volume of a rectangular parallelepiped is given by the product of its three side lengths, which can be expressed as $\operatorname{length} \otimes \operatorname{length} \otimes \operatorname{length}$.

In the case of probability measures, the product measure represents the independence of two random variables. For example, if we have two independent Bernoulli random variables with probability $p$, then the probability of observing a pair of outcomes $(t_1, t_2)$ is given by the product of the probabilities of observing each outcome individually, which can be expressed as $\operatorname{Bern}(p) \otimes \operatorname{Bern}(p)({t_1} \times {t_2}) = \operatorname{Bern}(p)({t_1}) \operatorname{Bern}(p)({t_2})$.

# **APPLYING A FUNCTION TO A MEASURE (THE PUSHFORWARD MEASURE)**

 If $\mu$ is a distribution on a set $X$ and $f: X \rightarrow Y$ is a function, it makes sense to consider the pushforward measure $f(\mu)$ as a distribution on the set $Y$.

To sample from the distribution $f(\mu)$, we can first sample from the distribution $\mu$ and then apply the function $f$ to the sample. This means that if we have a random variable $X$ with distribution $\mu$, and we define a new random variable $Y = f(X)$, then the distribution of $Y$ is given by $f(\mu)$.

The precise definition of the pushforward measure $f(\mu)$ is given by $f(\mu)(U) = \mu(f^{-1}(U)) = \mu({x \mid f(x) \in U})$, where $U \subseteq Y$ is a measurable set. This means that the measure of a set $U$ in the pushforward measure is equal to the measure of the preimage of $U$ under the function $f$ in the original measure.

The change of variable formula states that if $h(x)$ is the density of the measure $\mu$ and $h'(x)$ is the density of the pushforward measure $f(\mu)$, then for any measurable function $g(x)$, we have $\int g(x) h'(x) dx = \int g(f(x)) h(x) dx$. This formula is often used to compute the density of a transformed distribution in terms of the density of the original distribution.

**In this example,** you have a function $f(x) = x + 5$ and a standard normal distribution $\mu = N(0,1)$ on the real line. You want to find the distribution $f(\mu)$ on the real line.

To do this, you can first compute the cumulative distribution function (CDF) of $f(\mu)$. The CDF of $f(\mu)$ at a point $t$ is given by $f(\mu)(-\infty,t] = \mu({x \mid f(x) \le t}) = \mu({x \mid x + 5 \le t}) = \mu(-\infty, t-5]$.

To compute the probability density function (PDF) of $f(\mu)$, you can differentiate the CDF with respect to $t$. This gives you the formula $\frac{d}{dt} \int_{-\infty}^{t-5} \frac{1}{\sqrt{2 \pi \sigma^{2}}} e^{-\frac{x^{2}}{2 \sigma^{2}}} dx = \frac{1}{\sqrt{2 \pi \sigma^{2}}} e^{-\frac{(t-5)^{2}}{2 \sigma^{2}}}$.

As a result, you can see that the distribution $f(\mu)$ is indeed a normal distribution with mean 5 and standard deviation 1, as expected.
