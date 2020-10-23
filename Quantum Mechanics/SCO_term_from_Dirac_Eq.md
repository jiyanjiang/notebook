# Quantum Mechanics

## Q2: Show the origin of spin-orbit coupling from the relativistic Dirac equation.

In atomic physics, SCO comes from the relativistic Dirac equation, which reads:
$$
H_{SO} = \frac{1}{2m_0^2 c^2}\left( \frac{1}{r} \frac{\partial V}{\partial r} \right)  S \cdot L= \xi(r)S\cdot L
$$
Let's start from the time-independent Dirac equation: 
$$
\left( c \alpha \cdot p + \beta m_0 c^2 + V   \right) \psi = E \psi
$$
where, $ \alpha = \pmatrix{ 0 & \sigma \cr \sigma & 0  }, \beta = \pmatrix{ 1 & 0 \cr 0 & -1   } $.

Thus,
$$
\pmatrix{ m_0 c^2 + V & c \sigma \cdot p \cr c \sigma \cdot p & -  m_0 c^2 + V} \pmatrix{\psi_A \cr \psi_B} = E\pmatrix{\psi_A \cr \psi_B }
$$
or
$$
\cases{ (m_0 c^2 + V)\psi_A + c \sigma \cdot p \psi_B = E \psi_A  \\ c\sigma \cdot p \psi_A + (-m_0 c^2 + V)\psi_B = E \psi_B }
$$
Consider an electron is moving in an E-M field which is expressed via $(A_0, \vec A)$, in canonical quantization:  $p \to p - e \vec A, V \to V + eA_0$ (neglect other interactions except E-M interaction: $V = eA_0$),
$$
H = \frac{(\hat p - e \vec A)^2}{2m} + eA_0
$$

$$
\left[ \sigma \cdot \left( p - e A \right)  \right]\psi_B = \frac{1}{c} \left(E- eA_0 - m_0 c^2 \right)\psi_A \\ - \left[ \sigma \cdot \left( p - e A \right)  \right]\psi_A = - \frac{1}{c} \left( E - eA_0 + m_0 c^2 \right)\psi_B
$$
we can see that $\psi_A$ and $\psi_B$ are mixed, the normalization condition becomes:
$$
\int d^3 x \left( \psi_A^\dagger \psi_A + \psi^\dagger_B \psi_B \right)  = 1
$$
delete $\psi_B $ in expresion,
$$
\left[ \sigma \cdot \left( p - e A \right)  \right] \left[ \frac{c^2}{E-eA_0 + m_0 c^2} \right] \left[ \sigma \cdot \left( p - e A \right)  \right]  \psi_A \\=  \left[ E- eA_0 - m_0 c^2  \right] \psi_A
$$
Introduce $\tilde{E} $ in non-relativistic limit:
$$
\tilde{E} = E - m_0 c^2 \approx \frac{m_0 v^2}{2}+V \\= \frac{m_0 v^2}{2}+ e A_0
$$
Thus,
$$
\frac{c^2}{E-eA_0 + m_0 c^2} = \frac{1}{2m_0 }\left[1 - \frac{\tilde{E} - eA_0}{2 m_0 c^2  }  \right] \\ = \frac{1}{2m_0 } \left[ 1- \frac{1}{4} \cdot \frac{v^2}{c^2} \right]
$$
Negelect the $v^2/c^2$ term,
$$
\frac{1}{2m_0 } \sigma \cdot \left( p - eA \right)  \sigma \cdot \left( p - eA \right) \psi_A = \left( \tilde{E} - eA_0 \right) \psi_A
$$
Then, we get,
$$
\left[ \frac{1}{2m_0 } \left( p - eA \right)^2 + eA_0 - \frac{e \hbar}{2m_0 }\sigma \cdot B \right]\psi_A = \tilde{E} \psi_A
$$
Even in the non-relativistic limit, $A = 0, A_0 = 0, E = m_0 c^2$, the mixing does not vanish.
$$
\psi_B \approx \frac{\sigma \cdot p}{2m_0 c} \psi_A
$$
Normalized,
$$
\int d^3 x \left( \psi^\dagger_A \psi_A +  \psi_A^\dagger \left(  \frac{p^2}{4 m_0^2 c^2 } \right)  \psi_A \right) = 1
$$
Introduce new two component wave function:
$$
\Psi =\left( 1 + \frac{p^2}{8 m_0^2 c^2} \right)\psi_A  = \Omega \psi_A
$$
yields,
$$
\int d^3 x \Psi^\dagger \Psi = \int d^3 x \psi_A^\dagger \left[ 1 + \frac{p^2}{4 m_0^2 c^2}  \right] \psi_A = 1
$$
Consider $A=0, A_0 \neq 0$, From Eq(8), $\psi_A$ fulfills,
$$
H_A \psi_A = \\ \left[ \left( \sigma \cdot p \right) \frac{1}{2m_0}\left(1-  \frac{\tilde{E} - eA_0}{2m_0 c^2} \right) \left( \sigma \cdot p \right) + eA_0 \right] \psi_A  = \tilde{E} \psi_A
$$
In this expression, we have already considered the $v^2/c^2$ contribution. Now consider the wave equation:
$$
H_A \psi_A = \tilde{E} \psi_A
$$
Since, $\psi_A = \Omega^{-1}\Psi$
$$
H_A \Omega^{-1} \Psi = \tilde{E} \Omega^{-1}\Psi
$$
which means,
$$
\Omega^{-1} H_A \Omega^{-1}\Psi  = \tilde{E} \Omega^{-2}\Psi
$$
expand this equation and neglect orders higner than $v^2/c^2$,
$$
\left[ \frac{p^2}{2m_0} + eA_0 - \frac{p^4}{8 m_0^3 c^2} - \frac{e \hbar }{4 m_0^2 c^2}\sigma \cdot \left( \vec E \times \hat p \right) - \frac{e \hbar^2}{ 8 m_0^2 c^2} \nabla \cdot \vec E  \right] \Psi \\= \tilde{E}\Psi
$$
Since we have $A = 0$ assumption, there is no Zeeman term. The fourth term in this expression is the SCO term, which reads,
$$
- \frac{e \hbar }{4 m_0^2 c^2}\sigma \cdot \left( \vec E \times \hat p \right)
$$
where, 
$$
\vec E = - \nabla A_0 = -\frac{1}{e} \nabla \left( eA_0 \right) = - \frac{1}{e}\nabla V \\ = -\frac{1}{e}\hat e_r \frac{\partial V}{\partial r} = -\frac{1}{e} \frac{ \vec r}{r} \frac{\partial V}{\partial r}
$$
Plug into the SCO term,
$$
\frac{\hbar}{4 m_0^2 c^2 } \left( \frac{1}{r}\frac{\partial V}{\partial r} \right) \sigma \cdot  (\vec r \times \hat p ) = \frac{1}{2m_0^2 c^2}\left( \frac{1}{r} \frac{\partial V}{\partial r} \right)  S \cdot L
$$
Thus, we get the most often used SCO term.

