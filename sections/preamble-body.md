# The Preamble 
The Preamble is a very important piece of every LaTeX document. In the preamble you define the type of document you are writing, the language, and extra packages you will need, and set several parameters. Lets update the current Preamble that LaTeX has provided.

```
\documentclass{article}
\usepackage[utf8]{inputenc}

\title{My First LaTeX Project}
\author{Craig Waitt}
\date{October 2021}
```

Lets add some comments so we can define each package and lets add some special packages. Commenting in LaTeX is performed using the `%` symbol

```
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%         Preamble        %%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\documentclass[12pt, letterpaper]{article}     % What kind of document do we want to create
                                               % What size font and margins do we want to use
\usepackage[utf8]{inputenc}                    % This is the encoding for the document to allow 
                                               %    characters beyond ASCII (e.g.  à, ü, č ...) to be used

%%% User defined Packages %%%

\usepackage[english]{babel}                    % Optional language setting
\usepackage{amsmath}                           % Includes useful math symbols
\usepackage{tabularx}                          % Allows us to add tables
\usepackage{mhchem}                            % Writing chemical reactions, molecules, etc


%%% Document specific things %%%

\title{Hello World}                            % The title of your project            
\author{Craig Waitt}                           % Author name
\date{October 2021}                            % The date
```

Once you make some changes, hit `Recompile` button on the top left of the third window. If all runs well it should recompile the pdf based on the change of setting made in the Preamble. Before we look at the Body, lets look through the LaTeX document to add the package(s) to add figures to your LaTeX document.

## Exercise
**Add the package that allows us to include figures into our LaTeX document, as well as a folder in the project managment workspace (left window) that contains the path of where you will store your images. Click [here](soln1.md) for the solution.**

# The Body
Everything included inside the `\begin{document}` and `\end{document}` commands will be rendered in the final document.

```
\begin{document}

\maketitle

\section{Introduction}

\end{document}
``` 

The `\maketitle` command will read the title, author, and date info in the Preamble, and will render it at the begining of your document. From there, each subsequent section in your document will be seperated by the commands `\section{}` and `\subsection{}`. Next, we will go over several exercises you will come across in your writing.

[Chemical Formula >>>](chem-form.md)

[<<< Back](start.md)

[<<< Home](../README.md)
