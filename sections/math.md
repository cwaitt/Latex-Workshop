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

Gibbs free energy of formation: $\Delta G^{\circ}_{\text{form}} = \Delta H^{\circ}_{\text{form}} - \Delta S^{\circ}_{\text{form}} T$. This equation uses several \^ and \_ to set superscripts and subscripts. We are also using some mathematical symbols such as \textbackslash Delta ($\Delta$) and \textbackslash circ ($\circ$) which come from the \textbackslash usepackage\{amsmath\}. You'll notice that the mathematical symbols are italicized, but the word 'form' is not. Thats becasue we called the \textbackslash text\{\} command to force that word to show up in a regular font. It is very important to use `{}` appropriately to encapsulate parts of your equation. \\
\\
   
```

Copy this code into your LaTeX document and compile the PDF.


## Display Math Mode

Again, like inline math mode, there are three ways of calling display math mode:

1. `\[...\]'

2. `\begin{equation}...\end{equation}`

3. `\begin{displaymath}...\end{displaymath}


