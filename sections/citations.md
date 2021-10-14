# Making Citations

Adding citations into LaTeX is easy and seamless. The hard part is actually getting the things you want to cite into Overleaf, but citation managers such as Zotero and Mendeley have made it much easier to do so.

## Leraning Objectives

1. Creating a bib file

2. Calling a citation in text

3. Creating a References page 

## Bib Files

Bib files are formatted in 'LaTeX -like' style, where all you really need to know is the citation nickname. Below is an example of how the citations appear in a bib file. Make a file called sample.bib, in your project manager on the left, and copy this code into that file.

```
@article{ahu61,

   author={Arrow, Kenneth J. and Leonid Hurwicz and Hirofumi Uzawa},
   title={Constraint qualifications in maximization problems},
   journal={Naval Research Logistics Quarterly},
   volume={8},
   year=1961,
   pages={175-191}
}

@book{ab94,
   author* = {Charalambos D. Aliprantis and Kim C. Border},
   year = {1994},
   title = {Infinite Dimensional Analysis},
   publisher = {Springer},
   address = {Berlin}
}

@incollection{m85,
   author={Maskin, Eric S.},
   year={1985},
   title={The theory of implementation in {N}ash
 equilibrium: a survey},
   booktitle={Social Goals and Social Organization},
   editor={Leonid Hurwicz and David Schmeidler and Hugo Sonnenschein},
   pages={173-204},
   publisher={Cambridge University Press},
   address={Cambridge}
}

@inproceedings{ah2006,
   author={Aggarwal, Gagan and Hartline, Jason D.},
   year={2006},
   title={Knapsack auctions},
   booktitle={Proceedings of the 17th Annual ACM-SIAM Symposium on Discrete Algorithms},
   pages={1083-1092},
   publisher={Association for Computing Machinery},
   address={New York}
}

```

## Intext Citation

Once you have a citation file, you need to tell you LaTeX file to look for the bib file. Add the following two lines in the preamble:

```
\usepackage[backend=biber,style=chem-acs]{biblatex} % a package for writing citations

\addbibresource{sample.bib}
```

This tells LaTeX what kind of [citation style](https://www.overleaf.com/learn/latex/Biblatex_bibliography_styles) we want to use, and then the file that contains our citations.

Now that we have our citations loaded, we can start refering to them in text. To call a citation, you only need to use the `\cite{}` command. 

```
\newpage 

\section{Adding Citations}

Adding citations is easy. You only need to type what you want, followed by \textbackslash cite\{\} and the citation will appear.\cite{ab94} Overleaf, even creates a drop down menu for you to select which citation you want.\cite{ahu61} You can cite multiple sources at once as well.\cite{m85,ab94,ah2006}. You now no longer need to worry about properly citing each citation, {\LaTeX} takes care of it for you.
```
## References Page

Finally, you can display the bibliography by typing `\printbibliography` before the `\end{document}` line. Your references should now be displayed at the bottom of the document. You may wish to add a `\newpage` to separate the References from the rest of the document.

[Summary >>>](fin.md)

[<<< Back](figures.md)

[<<< Home](../README.md)


