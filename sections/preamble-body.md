# The Preamble and Body

## Learning Objectives

In this section, we will address and discuss the following:

1. Difference between the preamble and the body of a LaTeX document

2. Writing comments in your LaTeX document

3. Importing modules and setting document parameters in the preamble

4. Set up to begin writing content in the body

## The Preamble 

The preamble is a very important piece of every LaTeX document. In the preamble you define the type of document you are writing, the language, and extra packages you will need, and set several parameters. Lets look at the default preamble that LaTeX has provided. 

```
\documentclass{article}
\usepackage[utf8]{inputenc}

\title{My First LaTeX Project}
\author{Craig Waitt}
\date{October 2021}
```

There are five lines in this preamble. The first command, `\documentclass{article}`, tell LaTeX what kind of document you want to create. *Article* is the most common type of document, but there are several types of classes. *Report* is often used for longer documents with several chapters like a thesis, *letter* can be used for writting cover letters, *beamer* for writing presentations, and many others. 

`\usepackage[...]{...}` is a LaTeX command that allows us to import commands that are not standard in LaTeX (similar to *import* in python). There are more packages out there than anyone can count, and if there is something specific you want LaTeX to do, more often then not someone has wrote a package to do it for you. The `\usepackage[...]{}` command takes two arguements: (1) the name of the package you want to import enclosed in curly brackets '{}', and some options specific to the package enclosed in square brakets '[]'. For example, `\usepackage[utf8]{inputenc}` load the *inputenc* package and the option *utf8* tells LaTeX to interpret files using UTF8 encoding.

Following these two commands, we have three lines that define some document specific things, such as the document title, author, and date. All of these lines/commands can be changed and updated to reflect the type of document we want to make. Lets update the preamble and add some comments so we can define each package and lets add some special packages. Commenting in LaTeX is performed using the `%` symbol.

```
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%         Preamble        %%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\documentclass[12pt, letterpaper]{article}     % What kind of document do we want to create
                                               % What size font and margins do we want to use
\usepackage[utf8]{inputenc}                    % This is the encoding for the document to allow 
                                               %    characters beyond ASCII (e.g.  à, ü, č ...) to be used

%%% User defined Packages %%%

\usepackage{amsmath}                           % Includes useful math symbols
\usepackage{tabularx}                          % Allows us to add tables
\usepackage[version=4]{mhchem}                            % Writing chemical reactions, molecules, etc


%%% Document specific things %%%

\title{Hello World}                            % The title of your project            
\author{Craig Waitt}                           % Author name
\date{October 2021}                            % The date
```

Once you make some changes, hit `Recompile` button on the top left of the third window. If all runs well it should recompile the pdf based on the change of setting made in the preamble. Before we look at the body, lets look through the LaTeX document to add the package(s) to add figures to your LaTeX document.

### Exercise
**Add the package that allows us to include figures into our LaTeX document, as well as a folder in the project managment workspace (left window) that contains the path of where you will store your images. You can use the [Overleaf documentation](https://www.overleaf.com/learn) to do this, as well as any other documentation you find online. Click [here](soln1.md) for the solution.**

## The Body
Everything included inside the `\begin{document}` and `\end{document}` commands will be rendered in the final document.

```
\begin{document}

\maketitle

\section{Introduction}

\end{document}
``` 

The `\maketitle` command will read the title, author, and date info in the preamble, and will render it at the begining of your document. From there, each subsequent section in your document will be seperated by the commands `\section{}` and `\subsection{}`. Next, we will go over several exercises you will come across in your writing.

[Writing Mathematical Formula >>>](math.md)

[<<< Back](start.md)

[<<< Home](../README.md)
