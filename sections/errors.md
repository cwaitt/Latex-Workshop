# Identifying and Fixing Errors

## Learning Objectives

In this section, we will address and discuss the following:

1. How to identify errors in OverLeaf.

2. Fixing errors in OverLeaf.

## Identifying and Fixing Errors in OverLeaf

If you use another text editor or LaTeX distribution, you often have to go through some song and dance to identify the location of errors in the document. One of the overwheliming benefits of OverLeaf is its user friendly interactive environment, inluding highlight errors and their locations within the document. Lets start by writing some LaTeX code that will spit out some errors for us to look at. 

```
\section{Introduction}

This is my first {\LaTeX document. 

In this tutorial, we will discuss how to write mathematical equatons, tbls, and how to use the \includegraphics{} command.
```

There are two types of errors that LaTeX produces, *Errors* and *Warnings*. *Errors* are issues that LaTeX has detected that *prevent* the compilation of the pdf. *Errors* must be resolved before continuing. Most errors you come across are associated with the miss use of certain packages that you've loaded. In the example above, you'll notice a small red '1' at the top of the page, and a small red `x` in the LaTeX document. The red `x` tells you there is an error on this line, and what is causing the error. Additionally you can click the red `1` to open the log output which will tell you more specifics of the error. These errors can sometimes be hard to interpret, but the [OverLeaf documentation](https://www.overleaf.com/learn/latex/Errors) does a good job at explaining fairly common errors you'll run across. This error is telling me that "it cannot find a file to upload into the pdf", because I am using the backslash inappropriatly. LaTeX recognizes `\` as the start of a command, but I want to use it as text in this instance. So I will update the text as such:

```
\section{Introduction}

This is my first {\LaTeX document. 

In this tutorial, we will discuss how to write mathematical equatons, tbls, and how to use the \textbackslash includegraphics\{\} command.
```

The second type of error that LaTeX produces are *Warnings*. *Warning do not prevent* the compilation of the pdf. LaTeX sees a mistake in your code, and makes a guess on how to fix it. You should notice a yellow exclaimation mark on the line where the warning is raised. You may or may not also get a warning in the log file. You are not required to fix warnings, but warnings tend to slow down the compilation of the pdf so its recommended. LaTeX may have also guessed incorrectly what you meant so you may need to adjust the code to reflect what you wanted to type. In out little chunk of code, our warning is telling us we have an unenclosed curly brackey, so lets add the brakcet.

```
\section{Introduction}

This is my first {\LaTeX} document. 

In this tutorial, we will discuss how to write mathematical equatons, tbls, and how to use the \textbackslash includegraphics\{\} command.
```

Finally, you will notice there are several spelling mistankes in those two sentances. Remember LaTeX is a *What you type is what you mean* program, so if you misspell something LaTeX will just assume you wanted it to be that way. However, OverLeaf has its own separate spell-check that it will run in the background for you. If you click menu in the top left corner, there are several option you can control in your document, including the spell-check language. 

```
\section{Introduction}

This is my first {\LaTeX} document. 

In this tutorial, we will discuss how to write mathematical equations, tables, and how to use the \textbackslash includegraphics\{\} command.
```


[Writing Mathematical Formula >>>](math.md)

[<<< Back](preamble-body.md)

[<<< Home](../README.md)
