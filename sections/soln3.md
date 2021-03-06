# Writing Mathematical Formulae

```
\subsection{Exercise}

The rate expression is expressed as:
\begin{equation}
    \nu_{0} = k [\text{A}]^{x} [\text{B}]^{y}
    \label{eq:rate}
\end{equation}
where [A] and [B] are the concentration of species A and B respectively. $k$ is the rate constant, and the exponents ($x$ and $y$) are the partial rate orders. Equation \ref{eq:rate} can be found in any physical chemistry book.
\\
Assuming that this particular reaction is second order in A and zeroth order in B, the rate can be expressed as:
\begin{equation}
    \nu_{0} = k[\ce{A}]^{2}
\end{equation}
\noindent If the rate constant $k_{1}$ is known, then the concentration of \ce{A} at time $t$ can be computed by:
\begin{equation}
    \frac{1}{[\ce{A}]} = \frac{1}{[\ce{A}]_{0}} + kt
\end{equation}
```

After you write an equation, its important to maintain the font you used throughout your work. So if you wrote an equation in math mode, you should strive to maintain consistency and write those same symbols in math mode as well. Also use `\noindent` if you dont want LaTeX to indent your next paragraph.

[<<< Back](math.md)
