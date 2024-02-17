- [Weinberg-Witten Theorem](#weinberg-witten-theorem)
  - [Statement](#statement)
- [Notes](#notes)
  - [Introduction](#introduction)
  - [Classification of Particles from the Poincaré Group](#classification-of-particles-from-the-poincar%C3%A9-group)
  - [Proof](#proof)
  - [Consequences](#consequences)
    - [Bosons We Know](#bosons-we-know)
    - [No Background for Emergent Gravity](#no-background-for-emergent-gravity)
  - [Evading the Weinberg-Witten Theorem](#evading-the-weinberg-witten-theorem)
- [References](#references)


---


# Weinberg-Witten Theorem
## Statement
1. A theory containing a Poincaré covariant conserved four-vector current $J^\mu$ forbids masless particles of spin $j > 1/2$ with a non-vanishing eigenvalue of the conserved charge $Q = \int J^0 \mathrm{d}^3 x$.
    - **Construction mode**: A massless particle with spin $j > 1/2$ cannot carry a charge induced by a conserved Poincaré covariant four-vector current.
    - Contrapositive: If a massless charged particle of spin $j > 1/2$ exists, then the theory does not contain a Poincaré covariant conserved four-vector current $J^\mu$.
2. A theory containing a Poincaré covariant conserved energy-momentum tensor $T^{\mu \nu}$ forbids massless particles of spin $j > 1$ for which $\int T^{0 \nu} \mathrm{d}^3 x$ is the conserved energy-momentum four-vector.
    - **Construction mode**: A massless particle with spin $j > 1$ cannot carry energy-momentum induced by a conserved Poincaré covariant energy-momentum tensor.
    - Contrapositive: If a massless particle of spin $j > 1$ exists, then the theory does not contain a Poincaré covariant conserved energy-momentum tensor $T^{\mu \nu}$.

# Notes
## Introduction
- The proof heavily relies on Poincaré invariance. 
    - It can be considered as a fundamental reason for why we might have to leave the Minkowski background in order to search for an emergent theory of gravity.
## Classification of Particles from the Poincaré Group
- Poincaré group: A transformation $(\Lambda, a)$ is an element of the Poincaré group if it satisfies the following conditions:
    - $\Lambda$ is a Lorentz transformation.
    - $a$ is a translation.
    - The group composition law is given by
    $$
    (\Lambda_1, a_1) \cdot (\Lambda_2, a_2) = (\Lambda_1 \Lambda_2, \Lambda_1 a_2 + a_1).
    $$
- A transformation $(\Lambda, a)$ acts on a four-vector $x^\mu$ as
    $$
    x^\mu \to {x^\prime}^\mu = \Lambda^\mu_{~\nu} x^\nu + a^\mu.
    $$
- Poincaré algebra: The representation of the Poincaré group can be written infinitesimally as
    $$
    U(1+\omega, \epsilon) = 1 + \frac{\mathrm{i}}{2} \omega_{\mu \nu} M^{\mu \nu} - \mathrm{i} \epsilon_\mu P^\mu,
    $$
    where
    $$
    \begin{align*}
    \mathrm{i} [M^{\mu \nu}, M^{\rho \sigma}] &= \eta^{\nu \rho} M^{\mu \sigma} - \eta^{\mu \rho} M^{\nu \sigma} - \eta^{\nu \sigma} M^{\mu \rho} + \eta^{\mu \sigma} M^{\nu \rho}, \\
    \mathrm{i} [P^\mu, M^{\rho \sigma}] &= \eta^{\mu \rho} P^\sigma - \eta^{\mu \sigma} P^\rho, \\
    [P^\mu, P^\nu] &= 0, \\
    {M^{\mu \nu}}^\dagger &= M^{\mu \nu}, \\
    {P^\mu}^\dagger &= P^\mu, \\
    M^{\mu \nu} &= - M^{\nu \mu}.
    \end{align*}
    $$
- We define the Pauli-Lubanski vector as
    $$
    W^\mu = \frac{1}{2} \epsilon_{\mu \nu \rho \sigma} P^\nu M^{\rho \sigma}.
    $$
- Casimir operators: The only quadratic Casimir operators of the Poincaré algebra are
    $$
    \begin{align*}
    C_1 &= P_\mu P^\mu, \\
    C_2 &= W_\mu W^\mu.
    \end{align*}
    $$
 Each of $C_1$ and $C_2$ commutes with all other operators of the Poincaré algebra.
- The action of the Poincaré group on one-particle state vectors:
$$
\begin{align*}
C_1 |p, p^2, w^2, Z\rangle &= p^2 |p, p^2, w^2, Z\rangle, \\
C_2 |p, p^2, w^2, Z\rangle &= w^2 |p, p^2, w^2, Z\rangle, \\
P^\mu |p, p^2, w^2, Z\rangle &= p^\mu |p, p^2, w^2, Z\rangle.
\end{align*}
$$
- Representations: We use the little group to classify the representations of the Poincaré group. 
    $$
    U(\Lambda, 0) |p, p^2, w^2, Z\rangle = \left( \frac{N(p)}{N(\Lambda p)} \right) \sum_{Z^\prime} D_{Z^\prime Z}(B(\Lambda, p)) | \Lambda p, p^2, w^2, Z^\prime \rangle,
    $$
    where
    $$
    N(p) = \sqrt{\frac{k^0}{p^0}}
    $$
    and
    $$
    \omega_{\mu \nu} k^\nu = 0.
    $$
- **Massive representations**: For massive particles, the little group is $\mathrm{SO}(3)$, and
    $$
    \begin{align*}
    k^\mu &= (m, 0, 0, 0), \\
    C_3 &= - m^2 j(j-1) \cdot \mathbb{1}, \\
    |X\rangle &= |p, m^2, w^2, j, m\rangle.
    \end{align*}
    $$
- **Massless representations**: For massless particles, the little group is $\mathrm{ISO}(2) = \mathrm{SO}(2) \ltimes \mathrm{P}(2)$, and
    $$
    \begin{align*}
    k^\mu &= (E, 0, 0, E), \\
    C_3 &= 0, \\
    |X\rangle &= |p, j_3\rangle, \\
    U(\Lambda, 0) |p, j_3\rangle &= \sqrt{\frac{(\Lambda p)^0}{p^0}} \exp(\mathrm{i} j_3 \theta(\Lambda, p)) | \Lambda p, j_3\rangle.
    \end{align*}
    $$


## Proof
- The measuring process of charges is represented by approaching lightlike momentum transfer:
$$
\begin{align*}
\lim_{p^\prime \to p} \langle p^\prime, \pm j | J^0 | p, \pm j \rangle &= \frac{q}{(2\pi)^3}, \\
\lim_{p^\prime \to p} \langle p^\prime, \pm j | T^{0\nu} | p, \pm j \rangle &= \frac{p^\mu}{(2\pi)^3}.
\end{align*}
$$
Recall that
$$
\Lambda^\mu_{~0} = \frac{p^\mu}{|p|} = \frac{p^\mu}{E}.
$$
Then, 
$$
\begin{align*}
J^\mu &= \Lambda^\mu_{~0} J^0 = \frac{p^\mu}{E} J^0, \\
T^{\mu \nu} &= \Lambda^\mu_{~0} T^{0 \nu} = \frac{p^\mu}{E} T^{0 \nu}.
\end{align*}
$$
Therefore,
$$
\begin{align*}
\lim_{p^\prime \to p}
\langle p^\prime, \pm j | J^\mu | p, \pm j \rangle &= \frac{q p^\mu}{(2\pi)^3 E} \neq 0, \\
\lim_{p^\prime \to p}
\langle p^\prime, \pm j | T^{\mu \nu} | p, \pm j \rangle &= \frac{p^\mu p^\nu}{(2\pi)^3 E} \neq 0.
\end{align*}
$$
    - Note: We have massless particles, for which $p_\mu p^\mu = 0$, so
$$
\begin{align*}
\lim_{p^\prime \to p} 
\langle p^\prime, \pm j | P_\mu J^\mu | p, \pm j \rangle
&=
\lim_{p^\prime \to p}
-\mathrm{i} \hbar \langle p^\prime, \pm j | \partial_\mu J^\mu | p, \pm j \rangle
=
\frac{q p_\mu p^\mu}{(2\pi)^3 E} = 0, \\
\lim_{p^\prime \to p}
\langle p^\prime, \pm j | P_\mu T^{\mu \nu} | p, \pm j \rangle
&=
\lim_{p^\prime \to p}
-\mathrm{i} \hbar \langle p^\prime, \pm j | \partial_\mu T^{\mu \nu} | p, \pm j \rangle
=
\frac{p_\mu p^\mu p^\nu}{(2\pi)^3 E} = 0.
\end{align*}
$$
This means that $J^\mu$ and $T^{\mu \nu}$ are conserved tensors.
- For arbitary light-like $p$ and $p^\prime$, we have
$$
(p^\prime + p) = 2 |\mathbf{p}| |\mathbf{p}^\prime| (\cos(\phi) - 1) \leq 0,
$$
where $\phi$ is the angle between $\mathbf{p}$ and $\mathbf{p}^\prime$. We will consider the limit $p^\prime \to p$. 
    - For $\phi \neq 0$, we consider a frame in which
$$
p = (|\mathbf{p}|, \mathbf{p})
\quad\text{and}\quad
p^\prime = (|\mathbf{p}|, -\mathbf{p}).
$$
Note that a rotation by $+\theta$ around $\mathbf{p}$ is equivalent to rotation by $-\theta$ around $-\mathbf{p}$. Thus, under a rotation,
$$
\begin{align*}
|p, \pm j\rangle &\to \mathrm{e}^{\pm \mathrm{i} j \theta} |p, \pm j\rangle, \\
|p^\prime, \pm j\rangle &\to \mathrm{e}^{\mp \mathrm{i} j \theta} |p^\prime, \pm j\rangle. \\
\end{align*}
$$
Then,
$$
\begin{align*}
\langle p^\prime, \pm j| J^\mu(t, 0) |p, \pm j\rangle &\to \mathrm{e}^{\mp 2 \mathrm{i} j \theta} \langle p^\prime, \pm j| J^\mu(t, 0) |p, \pm j\rangle, \\
\langle p^\prime, \pm j| T^{\mu \nu}(t, 0) |p, \pm j\rangle &\to \mathrm{e}^{\mp 2 \mathrm{i} j \theta} \langle p^\prime, \pm j| T^{\mu \nu}(t, 0) |p, \pm j\rangle.
\end{align*}
$$
Meanwhile, under a rotation, $J^\mu \to R^\mu_{~\nu}(\theta) J^\nu$ and $T^{\mu \nu} \to R^\mu_{~\rho}(\theta) R^\nu_{~\sigma}(\theta) T^{\rho \sigma}$. Thus, we have
$$
\begin{align*}
\langle p^\prime, \pm j| J^\mu(t, 0) |p, \pm j\rangle &\to R^\mu_{~\nu}(\theta) \langle p^\prime, \pm j| J^\nu(t, 0) |p, \pm j\rangle, \\
\langle p^\prime, \pm j| T^{\mu \nu}(t, 0) |p, \pm j\rangle &\to R^\mu_{~\rho}(\theta) R^\nu_{~\sigma}(\theta) \langle p^\prime, \pm j| T^{\rho \sigma}(t, 0) |p, \pm j\rangle.
\end{align*}
$$
Therefore, equating the two expressions, we have
$$
\begin{align*}
\mathrm{e}^{\mp 2 \mathrm{i} j \theta} \langle p^\prime, \pm j| J^\mu(t, 0) |p, \pm j\rangle &= R^\mu_{~\nu}(\theta) \langle p^\prime, \pm j| J^\nu(t, 0) |p, \pm j\rangle, \\
\mathrm{e}^{\mp 2 \mathrm{i} j \theta} \langle p^\prime, \pm j| T^{\mu \nu}(t, 0) |p, \pm j\rangle &= R^\mu_{~\rho}(\theta) R^\nu_{~\sigma}(\theta) \langle p^\prime, \pm j| T^{\rho \sigma}(t, 0) |p, \pm j\rangle.
\end{align*}
$$
Note that $\Lambda(\theta)$ is a rotation matrix, so the eigvenvalues of this matrix can only be $\mathrm{e}^{\pm \mathrm{i} \theta}$ or $1$. This means that
$$
\begin{align*}
\lim_{p^\prime \to p} \langle p^\prime, \pm j| J^\mu(t, 0) |p, \pm j\rangle \neq 0 \quad &\text{unless} \quad 2j \in \{0, 1\}, \\
\lim_{p^\prime \to p} \langle p^\prime, \pm j| T^{\mu \nu}(t, 0) |p, \pm j\rangle \neq 0 \quad &\text{unless} \quad 2j \in \{0, 1, 2\},
\end{align*}
$$
or equivalently
$$
\begin{align*}
\lim_{p^\prime \to p} \langle p^\prime, \pm j| J^\mu(t, 0) |p, \pm j\rangle = 0 \quad &\text{for} \quad j > \frac{1}{2}, \\
\lim_{p^\prime \to p} \langle p^\prime, \pm j| T^{\mu \nu}(t, 0) |p, \pm j\rangle = 0 \quad &\text{for} \quad j > 1.
\end{align*}
$$
This **contradicts** the previous result that
$$
\begin{align*}
\lim_{p^\prime \to p}
\langle p^\prime, \pm j | J^\mu | p, \pm j \rangle &= \frac{q p^\mu}{(2\pi)^3 E} \neq 0, \\
\lim_{p^\prime \to p}
\langle p^\prime, \pm j | T^{\mu \nu} | p, \pm j \rangle &= \frac{p^\mu p^\nu}{(2\pi)^3 E} \neq 0.
\end{align*}
$$
Therefore, under the given assumptions, there cannot be any charged particles, i.e. $Q = \int J^0 \mathrm{d}^3 x \neq 0$ or $p^\mu = \int T^{0 \mu} \mathrm{d}^3 x \neq 0$, of spin $j > 1/2$ or $j > 1$ respectively.
    - For $\phi = 0$, under a rotation, we have
$$
\begin{align*}
|p, \pm j\rangle &\to \mathrm{e}^{\pm \mathrm{i} j \theta} |p, \pm j\rangle, \\
|p^\prime, \pm j\rangle &\to \mathrm{e}^{\pm \mathrm{i} j \theta} |p^\prime, \pm j\rangle.
\end{align*}
$$
Then, under a rotation, we have
$$
\begin{align*}
\langle p^\prime, \pm j| J^\mu(t, 0) |p, \pm j\rangle &\to \langle p^\prime, \pm j| J^\mu(t, 0) |p, \pm j\rangle, \\
\langle p^\prime, \pm j| T^{\mu \nu}(t, 0) |p, \pm j\rangle &\to \langle p^\prime, \pm j| T^{\mu \nu}(t, 0) |p, \pm j\rangle.
\end{align*}
$$
Evaluating the rotations as a Lorentz transformation applied to the tensors yields that
$$
\begin{align*}
\langle p^\prime, \pm j| J^\mu(t, 0) |p, \pm j\rangle &= R^\mu_{~\nu}(\theta) \langle p^\prime, \pm j| J^\nu(t, 0) |p, \pm j\rangle, \\
\langle p^\prime, \pm j| T^{\mu \nu}(t, 0) |p, \pm j\rangle &= R^\mu_{~\rho}(\theta) R^\nu_{~\sigma}(\theta) \langle p^\prime, \pm j| T^{\rho \sigma}(t, 0) |p, \pm j\rangle.
\end{align*}
$$
The right hand side depends on $\theta$, whereas the left hand side does not. This means that the components of teh matrix elements of $J^\mu$ and $T^{\mu \nu}$ along the dimension involved in the rotation must vanish for all helicities $j$. Nevertheless, the components of the matrix elements along $\mathbf{p}$ and $\mathbf{p}^\prime$ or the time axis do not have to vanish as their rotation eigenvalues are $1$. This shows that discontinuous currents are admitted.
        - We are only considering the limit $p^\prime \to p$, so the case $\phi = 0$ is not **relevant to the proof**. This is the limit of particles basically moving side by side along the same trajectory.

## Consequences
- The Weinberg-Witten theorem is a **no-go theorem** that states that if we want a massless particles with higher spin, we should not try to give it a charge induced by a Poincaré covariant conserved (vector or tensor) current.
    - We can evade the Weinberg-Witten theorem by having gauge particles, for which the corresponding currents are not Poincaré covariant due to the presence of gauges. This is one reason for why the success of gauge theories is not restrained by the Weinberg-Witten theorem.

### Bosons We Know
| Gauge boson | Spin | Electric Charge | Color Charge | Mass | Theory | Violation of Weinberg-Witten Theorem |
| --- | --- | --- | --- | --- | --- | --- |
| Photon $\gamma$ | $1$ | $\mathbf{0}$ | $\mathbf{0}$ | no | gauge | Chargeless |
| Weak W-boson $W^\pm$ | $1$ | $\mathbf{\pm 1}$ | $0$ | **yes** | gauge | Massive | 
| Weak Z-boson $Z^0$ | $1$ | $0$ | $0$ | **yes** | gauge | Massive |
| Gluons $\{g_k\}_{k=1}^8$ | $1$ | $0$ | $1$ | no | **gauge** | Not Charged under $J^\mu$ |
| Graviton $g$ | $2$ | $0$ | $0$ | no | **gauge** | Not Charged under $T^{\mu \nu}$ |
- **The gluon**. $J_a^\mu$ is not a current we can use in the context of the Weinberg-Witten theorem. The current only includes the quark fields, and therefore the gluon is not charged under the current:
$$
\left( \int J_a^0 \mathrm{d}^3 x \right) |p, \pm j\rangle = 0.
$$
- **The graviton**. The four-momentum of the graviton is not given by $\int T^{0 \nu} \mathrm{d}^3 x$, as
$$
T^{\mu \nu} = \frac{1}{\sqrt{-g}} \frac{\delta S}{\delta g_{\mu \nu}}.
$$
represents all the energy except for gravitational energy, and therefore, we can say that the graviton is not charged under the energy-momentum tensor.

### No Background for Emergent Gravity
-  We cannot compose a graviton from massless particles in Minkowski spacetime which are charged under a Lorentz covariant current.
    - If we would, for example, try to compose the spin $2$ graviton out of two spin $1$ gluons, the gluons
would contribute to a Lorentz covariant energy momentum tensor. This implies that their four-momentum can be described by $\int T^{0 \nu} \mathrm{d}^3 x$ Accordingly, the graviton would be charged under this tensor. This possibility for an emerging graviton was ruled out by the Weinberg-Witten theorem.
- The answer given by the Weinberg-Witten theorem is that a conventional theory living on a Minkowski background cannot mimic the properties of gravity.

## Evading the Weinberg-Witten Theorem
- **Noncommutative geometry**: An underlying noncommutative space
$$
[x^\mu, x^\nu] = \mathrm{i} \theta^{\mu \nu}
$$
naturally includes the idea of a diffeomorphism group with a semi-direct product structure, whereas this structure is not possible for an ordinary manifold. 
    - There are suggestions that in noncommutative spacetime, gravity could emerge from electromagnetism. The key point in this case is Lorentz invariance. Postulating noncommutative coordinates singles out special spacetime directions due to the presence of $\theta^{\mu \nu}$. It follows that the energy-momentum tensor in noncommutative geometry is not Lorentz covariant and according to the Weinberg-Witten theorem a graviton emerging from electromagnetism would be allowed.
- **AdS/CFT duality**: Our $3+1$ dimensional world could be a projection from a $2+1$ dimensional theory. All degrees of freedom are described by the lower dimensional theory. 
    - The idea was that the bound- ary of a very large region could be regarded as a flat plane at infinity. What we see in three dimensional space could be projected onto this distant screen which contains all necessary information to describe the bulk inside. 

# References
- S. Weinberg and E. Witten, Limits on massless particles. *Phys.Lett.B* 96 (1980) 59-62. DOI: [10.1016/0370-2693(80)90212-9](https://doi.org/10.1016/0370-2693(80)90212-9).
- F. Loebbert, The Weinberg-Witten Theorem on Massless Particles: *Annalen Phys.* 17 (2008) 803-829. DOI: [10.1002/andp.200810305](https://doi.org/10.1002/andp.200810305).
- L. Rozenberg, The Weinbberg-Witten Result for the Limits on Massless Particles: A Closer Look at the Proof. [https://acequark.github.io/notes/](https://acequark.github.io/notes/). 