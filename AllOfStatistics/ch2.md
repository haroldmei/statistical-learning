$\mathbb{V}$
${\rm I\!D}$
$\Omega$
$\bracevert_{0}^{infty}$
$\overset{above}{main}$
$\sim$
$\rightsquigarrow$
$\longrightarrow$

### Chapter 2

D2.1 Random variable: a mapping $ X : \Omega \Rightarrow \mathbb{R} $ that assigns a real number $X(\omega)$ to each outcome $\omega$  
E2.2 Flip a coin ten times. $X(\omega)$ is the number of heads in the sequence $\omega$ (an outcome).   
E2.3 Let $\Omega = {(x,y), x^2 + y^2 \le 1}$. Draw a point 'at random' from $\Omega$; the outcome $\omega = (x,y)$; examples of random variables $X(\omega)=x, Y(\omega)=y, W(\omega)=x+y, W(\omega)=x^2+y^2$.  
E2.4 Flip a coin twice and let X be the number of heads. $X(\omega)$ takes values 0, 1 and 2; The outcome $\omega$ is again a sequence of two head-tail combinations and there are 4 of them in the sample space $\Omega$.   
Let X be the random variable, x be a possible value of X, and A be a subset of the real line; define $X^{-1}(A) = {\omega \in \Omega: X(\omega) \in A}$  
$\mathbb{P}(X \in A) = \mathbb{P}(X^{-1}(A)) = \mathbb{P}({\omega \in \Omega; X(\omega) \in A})$  
$\mathbb{P}(X = x) = \mathbb{P}(X^{-1}(x)) = \mathbb{P}({\omega \in \Omega; X(\omega) = x})$  

D2.5 Cumulative distribution function CDF: $F_X: \mathbb{R} \rightarrow [0,1]$ s.t. $F_X(x) = \mathbb{P}(X \le x)$.  
E2.6 Flip a fair coin twice and let X be the number of heads. $\mathbb{P}(X=0) = \mathbb{P}(X=2) = 1/4, \mathbb{P}(X=1) = 1/2$. The CDF is   
$$ 
F_X(x) = 
\begin{cases}
  0     & \text{for } x < 0 \\
  1/4   & \text{for } 0\le x < 1 \\
  3/4   & \text{for } 1\le x < 2 \\
  1     & \text{for } x\ge 2
\end{cases}
$$

T2.7 Let X have CDF F, Y have CDF G. If F(x) = G(x) for all x, then $\mathbb{P}(X \in A)=\mathbb{P}(Y \in A)$ for all A.  
T2.8 $F:\mathbb{R} \rightarrow [0,1]$ is a CDF for some probability $\mathbb{P}$ iff   
1). F is non-decreasing.  
2). $\lim_{x \to -\infty} F(x)=0, \lim_{x \to \infty} F(x)=1$.  
3). F is right-continuous: $F(X)=F(X^+), where F(X^+)=\lim_{y \to x,y>x}F(y)$.  

D2.9 PMF probability mass function for discrete r.v. X is $f_X(x)=\mathbb{P}(X=x)$  
D2.11 PDF probability density function for continuous r.v. X is $f_X(x)=F_X'(x)$ at all points where its CDF is differentiable.  

E2.12 Given PDF for X: $f_X(x)=1 \text{for } 0\le x < 1$ otherwise 0, its CDF is given by
$$ 
F_X(x) = 
\begin{cases}
  0     & \text{for } x < 0 \\
  x     & \text{for } 0 \le x le 1 \\
  1     & \text{for } x > 1
\end{cases}
$$

E2.13 Given PDF for X: 
$$ 
f_X(x) = 
\begin{cases}
  0                     & \text{for } x < 0 \\
  \frac{1}{(1+x)^2}     & \text{for } x >= 0
\end{cases}
$$
Since $\int_{0}^{\infty} \frac{1}{(1+x)^2}dx = -\frac{1}{1+x} \bracevert_{0}^{\infty} = 1$, the PDF is well defined.

E2.14 Given a function for X: 
$$ 
f_X(x) = 
\begin{cases}
  0                 & \text{for } x < 0 \\
  \frac{1}{1+x}     & \text{for } x >= 0
\end{cases}
$$
Since $\int_{0}^{\infty} \frac{1}{1+x}dx = log(1+x) \bracevert_{0}^{\infty} = \infty$, it is not a valid PDF.

L2.15 Let F be the CDF for r.m. X;  
1). $\mathbb{P}(X=x)=F(x)-F(x^-)$;   
2). $\mathbb{P}(x<X \le y) = F(y)-F(x)$;   
3). $\mathbb{P}(X>x)=1-F(x)$;   
4). If X is continuous then $F(b)-F(a)=\mathbb{P}(a </\le X </\le b)$   

D2.16 Inverse of CDF F: $F^{-1}(q)=inf{x:F(x)>q} \forall q\in [0,1]$. If F is strictly increasing and continuous, then $F^{-1}(q)$ is the unique real x s.t. F(x)=q.  
Comments: the 'inf' definition could probably be replaced by 'sup' if we change the '>' to be '<'.   
Terms: first quartile, median, third quartile are defined by $F^{-1}(1/4), F^{-1}(1/2)$ and $F^{-1}(3/4)$  
equal in distribution: $X \overset{d}{=} Y$ if $\forall x, F_X(x)=F_Y(x) $  

Important random variables  
Point Mass: $\mathbb{P}(X=a) = 1$  
Discrete Uniform: $\mathbb{P}(X)=1/k, X \in {x_1, x_2, ..., x_k}$  
Bernoulli: $\mathbb{P}(X=1) = p, \mathbb{P}(X=0) = 1-p$, the PMF can be written as $f(x)=p^x(1-p)^1-x, \forall x \in [0,1]$  
Binomial: Flip coin n times, count heads. PMF takes values in {x \in \mathbb{R^+}, 0 \le x \le n}. The PMF is $f(x) = C_n^x p^x (1-p)^{n-x}, \forall x \in \mathbb{R^+}, 0 \le x \le n$, otherwise f(x) = 0.  
If $X_1 \sim Binomial(n1,p), X_2 \sim Binomial(n2,p), then X_1+X_2 \sim Binomial(n1+n2, p)$.

Geometric: $X \sim Geom(p)$ if $\mathbb{P}(X=k)=p(1-p)^{k-1}, k \ge 1$. Flip coins, the probability of getting a head on the kth coin.  
Poisson: $X \sim Poisson(\lambda)$ if $f(x)=e^{-\lambda} \frac {\lambda^x}{x!}, x \ge 0$. If $X1 \sim Poisson(\lambda1), X2 \sim Poisson(\lambda2)$, then $X1+X2 \sim Poisson(\lambda1+\lambda2)$.  
Continuous Uniform: $X \sim Uniform(a,b)$ if 
$$ 
f_X(x) = 
\begin{cases}
  \frac{1}{b-a}     & \text{for } x \in [a,b] \\
  0                 & \text{otherwise }
\end{cases}
$$

Normal (Gaussian):  $X \sim N(\mu, \delta^2)$ if $f(x)=\frac{1}{\delta \sqrt{2\pi}}e^{-\frac{(x-\mu)^2}{2\delta^2}}, x \in \mathbb{R}$  
Useful facts:  
1). If $X \sim N(\mu, \delta^2)$, then $Z = \frac{X-\mu}{\delta} \sim N(0,1)$.  
2). If $Z \sim N(0,1)$, then $X = \mu + \delta Z \sim N(\mu, \delta^2)$.  
3). If $X_i \sim N(\mu_i, \delta_i^2)$, i=1,2,...,n are independent, then $\Sigma_{i=1}^n X_i \sim N(\Sigma_{i=1}^n \mu_i, \Sigma_{i=1}^n \delta_i^2)$.  
4). $\mathbb{P}(a<X<b) = \mathbb{P}(\frac{a-\mu}{\delta}<Z<\frac{b-\mu}{\delta}) = \Phi(\frac{b-\mu}{\delta}) - \Phi(\frac{a-\mu}{\delta})$.  

Exponential: $X \sim Exp(\beta)$ if $f(x)=\frac{1}{\beta}e^{-x/\beta}, x>0$. The Exponential distribution is used to model the lifetimes of electronic components and the waiting times between rare events.  
Gamma: $X \sim Gamma(\alpha, \beta)$ if $f(x)=\frac{1}{\beta^\alpha \Gamma(\alpha)}x^{\alpha-1}e^{-x/\beta}, x>0$ where $\Gamma(\alpha)=\int_0^{\infty}y^{\alpha-1}e^{-y}dy$ is called 'Gamma function'. The Exponential distribution is just a Gamma distribution with $\alpha=1$  
Beta: $X \sim Beta(\alpha,\beta)$ if $f(x)=\frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)+\Gamma(\beta)}x^{\alpha-1}(1-x)^{\beta-1}, 0<x<1$.  
t and Cauchy: $X \sim t_\nu$ if $f(x)=\frac{\Gamma(\frac{\nu+1}{2})}{\Gamma(\frac{\nu}{2})} \frac{1}{(1+\frac{x^2}{\nu})^{(\nu+1)/2}}$. The t distribution with degree $\nu=\infty$ is Normal distribution. The Cauchy distribution is a special case of t with $\nu=1$  
Comments: The above mentioned t-distribution pdf seems to have something missing. Should be $f(x)=\frac{\Gamma(\frac{\nu+1}{2})}{\sqrt{\nu \pi} \Gamma(\frac{\nu}{2})} \frac{1}{(1+\frac{x^2}{\nu})^{(\nu+1)/2}}$  
Otherwise the Cauchy distribution pdf wouldn't be $f(x)=\frac{1}{\pi (1+x^2)}$ by making $\nu=1$ in t-distribution pdf.  

$\chi^2$ Distribution: X has a $\chi^2$ Distribution with p degrees of freedom written as $X \sim \chi_p^2$ if $f(x)=\frac{1}{\Gamma(p/2) 2^{p/2}} x^{p/2-1} e^{-x/2}, x>0$.  
If $Z_i$ with i=1,2,...,p are independent standard Normal r.v., then $\Sigma_{i=1}^p Z_i^2 \sim \chi_p^2$  

D2.19 PDF of joint r.v. (X,Y) is a function $f(x,y)$ where   
1). $\forall (x,y), f(x,y) \ge 0$  
2). $\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} f(x,y)dxdy = 1$  
3). for any set $A \subset \mathbb{R} \times \mathbb{R}, \mathbb{P}((X,Y) \subset A)=\iint_A f(x,y)dxdy$  
Similar definition applies to discrete r.v.  

D2.23 Marginal PMF of a joint discrete r.v. (X,Y) for X is defined as $f_X(x)=\mathbb{P}(X=x)=\sum_{y} \mathbb{P}(X=x,Y=y)=\sum_{y} f(x,y)$, marginal for Y is similar.  
D2.25 Marginal PDF of a joint continuous r.v (X,Y) is similarly defined by integral  

D2.29 Independent r.v. (X,Y), $\mathbb{P}(X,Y)=\mathbb{P}(X) \mathbb{P}(Y)$, $f_{X,Y}(x,y)=f_X(x)f_Y(y)$   
T2.34 Independence check: Suppose that the range of X and Y is a (possibly infinite) rectangle. If f(x,y)=g(x)h(y) for some functions g and h, not necessarily PDF, then X and Y are indenpent.  

D2.35 Conditional probability: Just remember $f_{X,Y}(x,y)=f_{X|Y}(x|y)f_Y(y)=f_{Y|X}(y|x)f_X(x)$ and $\mathbb{P}(X,Y)=\mathbb{P}(X) \mathbb{P}(Y|X) = \mathbb{P}(Y) \mathbb{P}(X|Y)$. The probablity of a given point for continuous is 0, how does the first one work?   