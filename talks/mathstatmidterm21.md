<head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head>

# Midterm Exam for *Mathematical Statistics (Honor)*, Fall 2021

Teacher: Fang YAO. Recalled and $\LaTeX$ed by: Wei GUO. **This version is not verbatim.**

## 1

Suppose that $(\xi_n,\eta_n)\sim_{\rm i.i.d.}{\cal N}(0,{\rm diag}\{\sigma^2,\tau^2\})$ for $n\ge 0$, where $\sigma,~\tau>0$ are constants. Let $X_0=0$, $X_{n+1}=a_nX_n+\xi_{n+1}$ and $Y_n=cX_n+\eta_n$ for $n\ge 0$, where $a_n,~c\ne 0$ are constants. Define

$$\widehat X_n=\mathbb{E}[X_n|Y_0,Y_1,...,Y_{n-1}],~P_n=\mathbb{E}(X_n-\hat X_n)^2,~n\ge 1.$$

1. Show that $\widehat X_{n+1}=a_n\left(\widehat X_n+\frac{cP_n}{c^2P_n+\tau^2}(Y_n-c\widehat X_n)\right)$.

2. Show that $P_1=\sigma^2$, $P_{n+1}=\sigma^2+a_n^2\frac{\tau^2P_n}{c^2P_n+\tau^2}$.

## 2

Suppose $(Y_{11i},Y_{12i},Y_{21i},Y_{22i})\sim\mathrm{Multinomial}\left(m;\frac{1+\theta_i}{4},\frac{1-\theta_i}{4},\frac{1-\theta_i}{4},\frac{1+\theta_i}{4}\right)$, $1\le i\le n$ are independent, where $m$ is given, and

$$\log\frac{1+\theta_i}{1-\theta_i}=\alpha+\beta x_i,~1\le i\le n,$$
where $\alpha,~\beta$ are unknown parameters, and $x_1,...,x_n$ are known constants.

1. Show that the joint distribution forms an exponential family, and find a minimal sufficient statistic.

2. It the statistic above complete or boundedly complete? Explain the reason.

## 3

Let $X_1,...,X_n$ be i.i.d. random variables, each having p.d.f. $f_\theta(x)=h(x)\exp(\theta T(x)-A(\theta))$, where $\theta\in\Theta\subset\mathbb{R}$ is unknown. Consider unbiased estimators for $\gamma(\theta)$ where $\gamma:\Theta\to\mathbb{R}$ is differentiable.

1. Find the C-R lower bound for the variance.

2. Show that the equality in (1) can be attained iff. $\gamma(\theta)=a\mathbb{E}_{\theta}T(X_1)+b$ for some $a,b\in\mathbb{R}$.

3. Determine the u.m.v.u.e. for $\mathbb{E}_{\theta}T(X_1)$ without using (2).

## 4

Let $X_1,...,X_n\sim_{\rm i.i.d.}{\cal N}(\mu,\sigma^2)$ where $\mu,\sigma^2$ are unknown. Consider estimating $\sigma^2$ under the squared error loss. Denote the sample variance as $S^2$.

1. Find the risk of $cS^2$ where $c>0$ is a constant. Show that the u.m.v.u.e. and the m.l.e. are inadmissible.

2. Find the m.l.e. under restriction $\mu\ge 0$, and determine its bias.

3. Find the Bayesian estimator w.r.t. the prior

   $$\frac{1}{\sigma^2}\sim\frac{1}{m\sigma_0^2}\chi_m^2,~\mu|\sigma^2\sim{\cal N}\left(\mu_0,\frac{\sigma^2}{\kappa}\right),$$
   where $\mu_0,\kappa,m,\sigma_0^2$ are prespecified. The p.d.f. of $\chi_m^2$ is
   $$x\mapsto\frac{1}{2^{\frac{m}{2}}\Gamma(\frac{m}{2})}u^{\frac{m}{2}-1}\exp\left(-\frac{u}{2}\right)\mathbb{I}_{x>0}.$$

## 5 (This problem did not appear on the test paper.)

Define $y\sim{\cal N}_p(\beta,\sigma^2I_p)$, $z\sim{\cal N}_p(\lambda\beta,\sigma^2I_p)$, and $s^2\sim\sigma^2\chi_q^2$, with unknown $\beta\in\mathbb{R}^{p}$, $\lambda\in\mathbb{R}$, and $\sigma>0$.

1. Find the m.l.e. for $\lambda$ and show that its mean squared error can be infinite.

2. Compute Jeffrey's prior on $(\lambda,\beta,\sigma^2)$ and show that the corresponding posterior expectation of $\lambda$ is the inverse regression estimator $\hat\lambda^{\rm I}=y'z/(s^2+||y||^2)$.

3. Using the reference prior technique, derive the corresponding posterior expectation $\hat\lambda^{\rm R}$ of $\lambda$.

4. Show that, as $q\to+\infty$, $\hat\lambda^{\rm I}\to_{\rm a.s.} 0$, but $\hat\lambda^{\rm R}$ is free of this inconsistency.

*Reminders*: Jeffrey's prior is given by $\pi(\theta)\propto\sqrt{\det{\cal I}(\theta)}$ where ${\cal I}(\theta)$ is the Fisher information matrix. When $x$ has pdf $f(x|\theta_1,\theta_2)$ where $\theta_1$ is the parameter of interest, the reference prior is obtained by first defining $\pi(\theta_2|\theta_1)$ as Jeffrey's prior associated with $f(x|\theta_1,\theta_2)$ when $\theta_1$ is fixed, then deriving the marginal p.d.f. $\tilde{f}(x|\theta_1)=\int f(x|\theta_1,\theta_2)\pi(\theta_2|\theta_1)\,{\rm d}\theta_2$, and computing Jeffrey's prior $\pi(\theta_1)$ associated with $\tilde{f}(x|\theta_1)$.
