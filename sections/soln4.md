# Thermodynamic Table

```
\subsection{Example}

\begin{table}[h]                % starts a table instance and places the table here! 
\begin{center}
\caption{Table of Thermodynamic data of 4 molecules.}       % A caption for the table
\begin{tabular}{ |c c c| }      % three columns, each with the text centered in each cell, and lines separating each column 
 \hline                 
\textbf{Molecule} & $\Delta H_{\text{form}}^{\circ}(298)$ (kJ mol$^{-1}$) & $S_{\text{form}}^{\circ}(298)$ (J mol$^{-1}$ K$^{-1}$) \\
\hline
\ce{CaO (s)} &  -635.09 & 39.75\\
\ce{CH3COOH(l)} & -276.98 &  160.67\\
\ce{Cl2(g) } & 0 & 223.06\\
\ce{Fe(CO)5 (l)} & -774.00 & 338.10\\
\hline
\end{tabular}
\label{tab:therm}
\end{center}
\end{table}
```

You can combine all different types of mode while typing in tables, which can be difficult in other software. One common mistake in making tables is forgetting the `\\` to tell LaTeX to start a new row. You'll also notice that the caption is very close to the table. You can increase the spaceing between a caption and the table. [How would you do that?](https://tex.stackexchange.com/questions/58674/the-space-between-the-table-and-its-caption-is-very-small)

[<<< Back](tables.md)
