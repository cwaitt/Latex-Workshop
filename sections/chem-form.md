# Writing Chemical Formula

There are a few LaTeX packages to create chemistry formulae: chemfig, mhchem, ochem, streetex, and xymtex. I am most familiar with mhchem (which is not in the overleaf documentation), but is fairly easy and straight foward to use. We loaded `\usepackage{mhchem}` in the Preamble, so lets go through some examples that use mhchem.

# Chemical Formulae

The mhchem package can be called by typing the command `\ce{}` in the body of your LaTeX document. Lets run through some examples of using mhchem. Change the `\section{Introduction}` command to `\section{Chemical Formulae}` and type beneath the following:

```
\section{Chemical Formulae}

You can write the combustion of propane (\ce{C3H8(g)}) in the presence of excess oxygen (\ce{O2 (g)}) producing carbon dioxide (\ce{CO2(g)}) and water (\ce{H2O(g)}). The balance chemical reaction can be written as:

\begin{center} % \begin{center} and \end{center} are used to center text in the document
\ce{C3H8(g) + 5O2(g) -> 3CO2(g) + 4H2O(g)}
\end{center}

You can also write general reactions such as:
\begin{center}
\ce{A-B + C* -> A* + B-C} \\ % the double slash forces a line break
\ce{NH3 + H+ <=> NH3-H^{\ddagger} -> NH4+}
\end{center}
```
