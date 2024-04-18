# Indiscrete note

# Fully expoiting a variational stability criterion

1d discrete

a series of damageable springs of given length $L$, with variable stiffness $\mu a(\alpha)$ depending on the local damage level $0\leq \alpha_i \leq 1$.

a chain of damageable springs of length $L$ is aligned and stretched along the  $x$ axis. The material of the bar has nominal stiffness (Young's modulus) $\mu$. We note $u_i$ the horizotal displacement of th $i$-th element. The structure is clamped at its ends, with imposed boundary displacements respectively
$$
\newcommand{\load}{\Delta}
u_0 = 0, u_N = \load
$$

Total energy of the bar is composed by two terms: one elastic (bulk) contribution and one damage (dissipation) which accounts for the energy spent to increase the damage level for each of the damaging springs.

$$
\begin{aligned}
\mathcal E_N (e, \alpha) &=  \sum_{i=0}^N \frac{1}{2} \mu   a(\alpha_i)  e_i^2  + \sum_{i=0}^N {w_1}w(\alpha_i) \
\tilde {\mathcal E}_N (u, \alpha) = \frac{1}{N} {\mathcal E}_N (u, \alpha) &=  \mu N\sum_{i=0}^N \frac{1}{2}  a(\alpha_i)  (u_i-u_{i-1})^2  + \frac{w_1}{N} \sum_{i=0}^N w(\alpha_i) 
\end{aligned}
$$

where the first integral is the strain energy and $W$ is the dissipated energy (per unit volume) due to damage and $\epsilon$ is the longitudinal strain.
The functions  $a(\alpha)$ and $w(\alpha)$ are non-dimensional functions, to be discussed later on.
As the boundary conditions are written with $u_{\{0, N\}}$, we need to include the constraint $\sum_i e_i = \Delta$ (CHECK)

#### Non-dimensionalisation

With no loss of generality we freely choose a unit length and a unit force (CHECK). We choose $L$ as unit length, and $\mu S$ (CHECK) as unit force/PRESSURE. We introduce non-dimesioal variables, denoted by a hat as follows

...

Dropping the hats, we are in a position to state 

The evolution problem
-   $\alpha \in [0,1] : \dot \alpha \geq 0$
    <!-- $E_N(\alpha) \leq E_N(\alpha + \beta) \quad \forall \beta \geq 0$ stability in the cone -->
- $E_N(y) \leq E_N(y + z) \quad \forall z = (v, \beta)\in K^+_0 := v \in \{ .. \}\times \beta \geq 0$ 
<!-- - power balance?  -->

the quantities $\alpha, \beta$ are vectors of $R^N$.

Remark: there is no power balance. (CHECK) what's missing?

The stability statement above
combination of two inequalities, one is "punctual" (holds for each of the elements indipendently), one is global and involves a scalar quantity that describes the whole structure. 
Extra attention is required for the space of admissible variations. In the statement above, the space  $K^+_0$ contains a singularity (?).
in the cone what does this mean?

- analytic
    the existence...
- numerically
    - frobenius theorem in 1d

## Solutions to Evolution

First variation

- mechanical equilibrium (displacements)

$$
\sigma'(\alpha(x), x) = 0 \\
+bcs \text{ on } \{0, L\}
$$

in 1d, a miracle happens: decoupling of the irreversible damage problem from the elastic (damageable) equilibrium problem. Constant stress throughout the bar allows to decouple/invert and get
$$
\sigma(\cdot, x) = \sigma(\bar \alpha)
$$
where $ \bar \alpha:= \max_x \alpha(x)$ is the maximum damage level (or something like this, to CHECK)

We finally obtain an energy which only depends on the values $\alpha_i$

- damage criterion

$$
\frac{N \mu}{2L^{2} N^{2}} {t^{2} \left. \frac{d}{d \beta} a{\left(\beta \right)} \right|_{ \beta=0 }} + \frac{1}{N}{\left. \frac{d}{d \beta} w{\left(\beta \right)} \right|_{ \beta=0 }}\geq 0
$$
- equilibrium solution
    - elastic phase ($\alpha(x) =0$)
    - damaging phase ($\alpha(x) >0$)

        Solving the damage criterion yields solutions 
        $$
        \alpha_t: t\mapsto 
        $$

Qualitative analysis of solutions:
    - homogeneous solutions
        $$
        \alpha_t: \alpha_t'(x)=0 \\  
        \alpha_t: \alpha_i=\alpha\in \R, \quad \forall i  
        $$
    - localisations
        $$
        \alpha_t: \alpha_t'(x)\neq0 \\  
        \alpha_t: \exists \text{ at least one index } j \in \{0, N\}: \alpha_i\neq\alpha_j, \quad \forall i  
        $$
    
### Second variation
#### Bifurcations

The solution to this problem responds to the question: is the current evolution path unique?
This is a "rate problem" in the sense that it is formulated taking variations with respect to the rate of change of the state variables, not on the state variables itself.

Assuming continuity with respet to time of the evolution maps (CHECK) the variational problem of bifurcation is written by (formally?) derivating with respect to time the ...

Computing ...
the bifurcation problem (1d discrete) writes as follows:

$$
eigen problem: E_N''(y_t)(\dot z, \dot z) \geq 0, \forall \dot z\in V 
$$
where $V$ is a Sobolev space which has vector structure.

Competition between solutions such that $m$ out of $N$ ($m < N$) springs bifurcate simultaneously, thus $N-m$ springs remain at given damage $\alpha^*$. 

The energy of the bifurcating system is

evolution for the $m$ springs $\alpha_t$ solves first order optimality condition

Whenever the inequality in [bif] is verified with the strict sign the evolution traced by the rate $\dot y_t$ is unique (thus stable hence observable), whereas when equality occurs, the Hessian $E''_N$ is singular and, as such, allows for the existence of path-bifurcations.  
Accordingly, the bifurcation load is given by the following eigenvalue problem 






#### Stability

Conceptually different from the bifurcation criterion is the implication of the stability criterion at order two, yielding the following inequality (which we refer to as the stability criterion).
The stability criterion is given by the following inequality

Whenever the criterion is verified with the strict ineqality, then the state $y_t$ is at a local constrained energy-minimum, whereas when the equality occurs there exist nontrivial directions (the eigenfunctions associated to negative eigenvectors) along which the energy can decrease. As such, the state $y_t$ is unstable.  



Remarks on the 1d case:

- N = $\bar N$ implies the existence of a lengthscale, to model a real bar of length $L$, it is $\ell = L/\bar N$ 




##### Analytic result:
Existence of stable evolutionary paths, in the discrete case, both in 1d and 2d.

There exist $y_t: t\mapsto $





#### 3 models, compared

To analyse the effect of softening on the strength, we consider three specific parametric material model characterized by degradation functions which enjoy different qualitative properties

### At1

For AT1 model, the relation between the imposed load and S (CHECK) reads $\Delta = S  (1-\alpha_i)^{3/2}$ and (the diagonal terms of the Hessian matrix read $H_{ii} = c  (-(1-\alpha_i)^2  S + (4/3) h)$. 
For the branch of homogeneous solutions, we can evaluate $S=(1-\alpha_H)^{-2}$ and hence $H_{ii} = c (-1 + (4/3) h)$ thus stability holds only for $N<4/3$ !.
But for other branches, a formula for $H_{ii}$ involving  only $\Delta$, as (\ref{eq:Hii_LS_bis}), does not exist.


### At2

### LS

$$
    a(\alpha) := \frac{1-w(\alpha)}{1 + \left(\gamma-1\right)w(\alpha)}  ,
    \qquad
    w(\alpha) := 1 - (1-\alpha)^2
$$
A close inspection reveals that this model enjoys the following properties:
- Strain hardening if and only if $\gamma>1$; 
- Stress softening for any $\gamma>0$;
- Maximum allowable stress $\sigma_c$ and strain for elastic limit $\varepsilon_c$ are given by:

$$\sigma_c:=\sqrt{\dfrac{2\mu w_1 }{\gamma}}
 , \quad
\varepsilon_c:=\sqrt{\dfrac{2 w_1 }{\mu \gamma}}
$$

NB: we will choose $w_1 = \gamma \mu / 2$ with no loss of generality.




The evolution of stress, strain, and damage under monotonically increasing displacement-controlled loading, where the response is uniform (homogenous) $\varepsilon L=\Delta$, the response is purely elastic for 
$\Delta \leq  \varepsilon_c = \sqrt{2w_1/(\mu  \gamma)}$, where the damage criterion is not still attained. For $\Delta \geq  \varepsilon_\infty := \sqrt{2w_1 \gamma / \mu}$ the full damage level is attained and the stress is zero. For intermediate value, the damage is found by solving for the damage criterion as an equality. This gives the following strain-stress relations



\[
\begin{cases}
   \sigma = \mu \,{\varepsilon}, &\text{ if } {\varepsilon} \leq \varepsilon_c \, , \\
    %
    \sigma = \mu\left({\varepsilon} -\sqrt{\frac{2w_1 \gamma}{\mu }}\right), 
    &\text{ if } 
   \varepsilon_c    \leq    \varepsilon \leq    \varepsilon_\infty,    \\
    %
    \sigma=0, 
    &\text{ if } 
    \varepsilon_\infty \leq  \varepsilon.\\
\end{cases}   
\]

Remark: Adopting the non-dimensionalisation above we get $\sigma_c=1$, $\varepsilon_c=1$, and $\varepsilon_\infty=\gamma$.




We note $S:=\int_0^1 s(\alpha(x)) dx = h \, \sum_i s(\alpha_i)$.


The second variation in ... can then be written in matrix form as
\[
\begin{align}
\text{ for } i \neq j: \, H_{ij} = \Delta^2 \, h^2 \,  \frac{s'(\alpha_i) \, s'(\alpha_j)}{S^3} \\
%
H_{ii} = h\, W w''(\alpha_i) - \frac{\Delta^2}{2} \, h \,  \frac{s''(\alpha_i)}{S^2}  + \Delta^2 \, h^2 \,  \frac{s'(\alpha_i)^2}{S^3} 
\end{align}
\]

And the condition ... can be written as
\[
\forall  \beta_i , \beta_j >0  : \sum_{i,j} H_{ij} \, \beta_i \, \beta_j >0
\]

this condition is fulfilled iff 
\[
\begin{align}
\forall  i  &:  0 < H_{ii}  \\
\text{and } \forall  i \neq j  &:  - \sqrt{H_{ii} H_{jj} } < H_{ij}
\end{align}
\]


which seems to be related to the Perron-Froebenius theorem.
Perron-Froebenius theorem says that if a matrix has all its entries $>0$, then it admits an eigenvector with only $>0$ components. The associated eigenvalue is $>0$ and is equal to the spectral radius of the matrix (max of the module of all eigenvalues).




In this section, we show that {\em all} equilibrium branches loose stability when $\Delta=h \, \gamma$.
Please note that for an index $i$ experiencing damage, we have

$$
\begin{align}
\frac{\gamma}{2} \, \left( 1 - \frac{1}{(1-\alpha)^2} \, \frac{\Delta^2}{S^2} \right)=0 \\
\text{ that is } \Delta = (1-\alpha_i) \, S(\alpha_1, \alpha_2, \ldots, \alpha_N) 
\end{align}
$$


Please also note that ... writes
$$
\begin{align}
H_{ii} = \frac{h \, \Delta^2 \gamma}{S^3 (1-\alpha_i)^4} \left( -(1-\alpha_i) S(\alpha_1, \alpha_2, \ldots, \alpha_N) + h \gamma \right)
\end{align}
$$

#### The loss of stability of the homogeneous branch

On this branch we have $\alpha_i = \alpha_H$ for all $i$.
Hence $S=h \sum_i s(\alpha_i) = h N s(\alpha_H)=s(\alpha_H)$.
For each $i$, ... holds.
All diagonal terms in the Hessian matrix are the same, and ... with .... yields
$$
\begin{align}
H_{ii} = \frac{h \, \Delta^2 \gamma}{S^3 (1-\alpha_H)^4} \left( -\Delta + h \gamma \right)
\end{align}
$$
So the loss of stability happens when $\Delta = h \gamma$.

In general, on a branch with $i$ damaging springs and $j$ passive springs, we have that all the $\alpha_i$ attain the same value (because of history), and all the $\mu_j>0$ (because the value of $\sigma=\Delta/S$ has decreased since this $j$ was damaging, see ...). 
Hence the stability test has to be carried  only for indices $i$, which yields the same relation as above.


----------------

Provide notebook playground


Remark: 1d (miracle): transparent solution $\sigma$

difference, big Hessian, small Hessian

* extra 1 argument
* extra 2 argument

Finite elements, 
the genral case

another miracle in 2d (with substrate)

- analytic computation
- numeric implementation with "small" $N$, (i.e. $N\sim 64$)

then $\bar N$ implies $\bar \ell$

#### Ouverture:

in the continuum case, add a term $\ell^2 |\alpha '|^2$

(LS: continuation along branch)

Applications:
    - economic game theory