# Writing Mathematical Formula

LaTeX makes writing chemical equations seamlessly. There are two ways you will likely use math mode: *inline* math mode, which allows you to write equations as a part of a paragraph, and *display* math mode, which is used to write equations that are not part of a paragraph.

## Inline Math Mode

There are three ways to start up inline math mode:

1. `\(...\)`

2. `$...$`

3. `\begin{math} ... \end{math}`

My preference for calling inline math mode is to use `$...$` since I'm not using the `$` sign often in text, and requires less user input. 

Lets try some examples of inline math mode.

```
\section{Math Mode}

\subsection{Inline Math Mode}

Gibbs free energy of formation: $\Delta G^{\circ}_{\text{form}} = \Delta H^{\circ}_{\text{form}} - \Delta S^{\circ}_{\text{form}} T$. This equation uses several {\string^} and {\_} to set superscripts and subscripts. We are also using some mathematical symbols such as \textbackslash Delta ($\Delta$) and \textbackslash circ ($\circ$) which come from the \textbackslash usepackage\{amsmath\}. You'll notice that the mathematical symbols are italicized, but the word 'form' is not. That's because we called the \textbackslash text\{\} command to force that word to show up in a regular font. It is very important to use `\{\}` appropriately to encapsulate parts of your equation. \\
\\ 
```

Copy this code into your LaTeX document and compile the PDF.


## Display Math Mode

Again, like inline math mode, there are three ways of calling display math mode:

1. `\[...\]`

2. `\begin{equation}...\end{equation}`

3. `\begin{displaymath}...\end{displaymath}`

My preference for display mathmode is to use `\begin{equation}...\end{equation}`

Lets add another example into our LaTeX document.

```
\subsection{Display Mode}

The canonical partition function can be expressed as:
\begin{equation}
    Z = \sum_{i} \exp(-\epsilon_{i}\beta)
\end{equation}
\noindent or:
\begin{equation}
    Z = \sum_{i} \exp(\frac{-\epsilon_{i}}{k_{b}T})
    \label{eq:partfunc}
\end{equation}

We can refer to equations in display mode later by assigning it a label and the calling it by typing \textit{\textbackslash ref\{\}}. So now I can say equation \ref{eq:partfunc} is the canonical partition function. Now if you choose to reorganize the equations later, as long as you carry the label, the text will update accordingly. Try switching the order of the two equations and recompile to see what happens.

```

The `\label{}` command is very powerful as it allows you to refer to the equations (as we will see figures and tables) without worring about the order which they appear.

## Exercise
**Try reproducing the the following bellow in you LaTeX Document. You may find this external sheet helpful when looking up [math symbols](https://www.overleaf.com/learn/latex/Mathematical_expressions#Reference_guide), or this one which is a more comprehensive [list of symbols](https://www.caam.rice.edu/~heinken/latex/symbols.pdf).**

![math](/images/Math-Eq.png)

The solution can be found [here](soln3.md).

[Creating Tables >>>](tables.md)

[<<< Back](chem-form.md)

[<<< Home](../README.md)
