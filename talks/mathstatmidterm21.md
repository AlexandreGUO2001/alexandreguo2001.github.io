$$\newcommand{\ro}[1]{\left(#1\right)} % round brackets (parentheses)
\newcommand{\sq}[1]{\left[#1\right]} % square brackets (brackets)
\newcommand{\cu}[1]{\left\{#1\right\}} % curly brackets (braces)
\newcommand{\abs}[1]{\left\vert#1\right\vert}
\newcommand{\norm}[2]{\left\Vert#1\right\Vert_{#2}}
\newcommand{\ee}{\mathrm{e}}
\newcommand{\pif}{{+\infty}}
\newcommand{\tp}{^{\mathrm{T}}}
\newcommand{\const}{{\textrm{const}}}
\newcommand{\p}[2]{\,\mathbb{P}_{#1}\left(#2\right)}
\newcommand{\e}[2]{\,\mathbb{E}_{#1}\left[#2\right]}
\newcommand{\var}[2]{\,\mathbb{V}\mathrm{ar}_{#1}\left[#2\right]}
\newcommand{\cov}[2]{\,\mathbb{C}\mathrm{ov}_{#1}\left(#2\right)}
\newcommand{\I}[1]{\,\mathbb{I}_{\left\{#1\right\}}}
\newcommand{\iid}{\stackrel{\textsc{i.i.d.}}{\sim}}
\newcommand{\iidtext}{\textsc{i.i.d.}}
\newcommand{\pdf}{\textsc{p.d.f.}}
\newcommand{\cdf}{\textsc{c.d.f.}}
\newcommand{\R}[1]{{\mathbb{R}^{#1}}}
\newcommand{\n}[2]{{\cal N}_{#1}\left(#2\right)}
\newcommand{\ber}[1]{{\rm Bernoulli}\left(#1\right)}
\newcommand{\be}[1]{{\rm B}\left(#1\right)}
\newcommand{\asto}{\stackrel{\text{a.s.}}{\longrightarrow}}
\newcommand{\dd}{{\rm \,d}}
\newcommand{\de}[2]{\frac{{\rm d}#1}{{\rm d}#2}}
\newcommand{\dde}[2]{\frac{{\rm d}^2#1}{{\rm d}#2^2}}
\newcommand{\pd}[2]{\frac{\partial#1}{\partial#2}}
\newcommand{\ppd}[2]{\frac{\partial^2#1}{\partial#2^2}}
\newcommand{\pppd}[3]{\frac{\partial#1}{\partial#2\partial#3}}
\newcommand{\pdr}[3]{\frac{\partial^{#3}#1}{\partial#2^{#3}}}
\newcommand{\Ica}{{\mathcal{I}}}$$

# Midterm Exam for *Mathematical Statistics (Honor)*, Fall 2021

Teacher: Fang YAO. Recalled and $\LaTeX$ed by: Wei GUO.

***This version is not verbatim.***

## 1

Suppose that $(\xi_n,\eta_n)\iid\n{}{0,\diag{\sigma^2,\tau^2}}$ for $n\ge 0$, where $\sigma,~\tau>0$ are constants. Let $X_0=0$, $X_{n+1}=a_nX_n+\xi_{n+1}$ and $Y_n=cX_n+\eta_n$ for $n\ge 0$, where $a_n,~c\ne 0$ are constants. Define

$$\widehat X_n=\e{}{X_n|Y_0,Y_1,...,Y_{n-1}},~P_n=\e{}{(X_n-\hat X_n)^2,~n\ge 1.$$

1.  Show that $\widehat X_{n+1}=a_n\left(\widehat X_n+\frac{cP_n}{c^2P_n+\tau^2}(Y_n-c\widehat X_n)\right)$.

2. Show that $P_1=\sigma^2$, $P_{n+1}=\sigma^2+a_n^2\frac{\tau^2P_n}{c^2P_n+\tau^2}$.


## 2

Suppose $(Y_{11i},Y_{12i},Y_{21i},Y_{22i})\sim\mathrm{Multinomial}\left(m;\frac{1+\theta_i}{4},\frac{1-\theta_i}{4},\frac{1-\theta_i}{4},\frac{1+\theta_i}{4}\right)$, $1\le i\le n$ are independent, where $m$ is given, and

$$\log\frac{1+\theta_i}{1-\theta_i}=\alpha+\beta x_i,~1\le i\le n,$$
where $\alpha,~\beta$ are unknown parameters, and $x_1,...,x_n$ are known constants.

1. Show that the joint distribution forms an exponential family, and find a minimal sufficient statistic.

2. It the statistic above complete or boundedly complete? Explain the reason.

## 3

Let $X_1,...,X_n$ be \iidtext~random variables, each having \pdf~$f_\theta(x)=h(x)\exp(\theta T(x)-A(\theta))$, where $\theta\in\Theta\subset\R{}$ is unknown. Consider unbiased estimators for $\gamma(\theta)$ where $\gamma:\Theta\to\R{}$ is differentiable.

1. Find the C-R lower bound for the variance.

2. Show that the equality in (1) can be attained iff. $\gamma(\theta)=a\e{\theta}{T(X_1)}+b$ for some $a,b\in\R{}$.

3. Determine the UMVUE for $\e{\theta}{T(X_1)}$ without using (2).


## 4
Let $X_1,...,X_n\iid\n{}{\mu,\sigma^2}$ where $\mu,\sigma^2$ are unknown. Consider estimating $\sigma^2$ under the squared error loss. Denote the sample variance as $S^2$.

1. Find the risk of $cS^2$ where $c>0$ is a constant. Show that the UMVUE and the MLE are inadmissible.

2. Find the MLE under restriction $\mu\ge 0$, and determine its bias.

3. Find the Bayesian estimator w.r.t. the prior

    $$\frac{1}{\sigma^2}\sim\frac{1}{m\sigma_0^2}\chi_m^2,~\mu|\sigma^2\sim\n{}{\mu_0,\frac{\sigma^2}{\kappa}},$$
    where $\mu_0,\kappa,m,\sigma_0^2$ are prespecified. The \pdf~of $\chi_m^2$ is 
    $$x\mapsto\frac{1}{2^{\frac{m}{2}}\Gamma(\frac{m}{2})}u^{\frac{m}{2}-1}\ee^{-\frac{u}{2}}\I{x>0}.$$

## 5 (This problem did not appear on the test paper.)

Define $y\sim\n{}{\beta,\sigma^2I_p}$, $z\sim\n{}{\lambda\beta,\sigma^2I_p}$, and $s^2\sim\sigma^2\chi_q^2$, with unknown $\beta\in\R{p}$, $\lambda\in\R{}$, and $\sigma>0$.

1. Find the MLE for $\lambda$ and show that its mean squared error can be infinite.

2. Compute Jeffrey's prior on $(\lambda,\beta,\sigma^2)$ and show that the corresponding posterior expectation of $\lambda$ is the inverse regression estimator $\hat\lambda^{\rm I}=y\tp z/(s^2+\norm{y}{}^2)$.

3. Using the reference prior technique, derive the corresponding posterior expectation $\hat\lambda^{\rm R}$ of $\lambda$.

4. Show that, as $q\to\pif$, $\hat\lambda^{\rm I}\asto 0$, but $\hat\lambda^{\rm R}$ is free of this inconsistency.

*Reminders*: Jeffrey's prior is given by $\pi(\theta)\propto\sqrt{\det\Ica(\theta)}$ where $\Ica(\theta)$ is the Fisher information matrix. When $x$ has pdf $f(x|\theta_1,\theta_2)$ where $\theta_1$ is the parameter of interest, the reference prior is obtained by first defining $\pi(\theta_2|\theta_1)$ as Jeffrey's prior associated with $f(x|\theta_1,\theta_2)$ when $\theta_1$ is fixed, then deriving the marginal \pdf~$\tilde{f}(x|\theta_1)=\int f(x|\theta_1,\theta_2)\pi(\theta_2|\theta_1)\dd\theta_2$, and computing Jeffrey's prior $\pi(\theta_1)$ associated with $\tilde{f}(x|\theta_1)$.
