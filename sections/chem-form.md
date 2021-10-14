# Writing Chemical Formula

There are a few LaTeX packages to create chemistry formulae: chemfig, mhchem, ochem, streetex, and xymtex. I am most familiar with mhchem (which is not in the overleaf documentation), but is fairly easy and straight foward to use. We loaded `\usepackage{mhchem}` in the preamble, so lets go through some examples that use mhchem.

## Learning Objectives

1. Write chemical formula with mhchem

2. Write in text as well as equations

# Chemical Formulae

The mhchem package can be called by typing the command `\ce{}` in the body of your LaTeX document. Lets run through some examples of using mhchem.

```
\newpage 

\section{Chemical Formulae}

You can write the combustion of propane (\ce{C3H8(g)}) in the presence of excess oxygen (\ce{O2 (g)}) producing carbon dioxide (\ce{CO2(g)}) and water (\ce{H2O(g)}). The balance chemical reaction can be written as:

\begin{center} % \begin{center} and \end{center} are used to center text in the document
\ce{C3H8(g) + 5O2(g) -> 3CO2(g) + 4H2O(g)}
\end{center}

You can also write general reactions such as:
\begin{center}
\ce{A-B + C* -> A* + B-C} \\
\ce{A + B <=> [A-B]}
\end{center}

After compiling {\LaTeX} should have formatted your chemical formulae for you. % \LaTeX is a built-in command for writting the word LaTeX correctly. We encapsulate \LaTeX in {} to put a space between the words 'LaTeX' and 'should'. Delete the {} brackets and recompile the file to see what happens.

```

After you add the following to check that the code was entered correctly. You should see beautifully formated chemical equations. The mhchem package can be commbined with math mode symbols (next section) to make even nicer chemical equations. You can use the [mhchem documentation](https://mirror.las.iastate.edu/tex-archive/macros/latex/contrib/mhchem/mhchem.pdf) to format more complex chemical equations.

## Exercise
**Try reproducing the follwoing equations in LaTeX. The solution can be found [here](soln2.md).**

![chemeq](/images/Chem-Eq.png)


[Creating Citations >>>](citations.md)

[<<< Back](figures.md)

[<<< Home](../README.md)

