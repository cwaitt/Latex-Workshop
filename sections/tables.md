# Making Tables

Make tables in LaTeX can be a somewhat tedius task (as compared to Google Sheets or Excel), but there are external applications you can use to convert you [excell sheet into LaTeX format](https://tableconvert.com/). If you use python to make your tables, there is even a conveinent module in [pandas](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_latex.html) to convert your tables into LaTex. This page will use the `\usepackage{tabularx}` package to make some small simple tables from scratch.

## Table Format
The `\usepackage{tabularx}` package takes a second set of curly brakets that tells LaTeX how many columns are in your table, as well as how to center the test and how to draw verticle lines. For example, Lets say we want to make a table of containing three columns that are seperated by verticle lines. This can be acheived by:

```
\section{Making Tables}

\begin{table}[h]                % starts a table instance and places the table here! 
\begin{center}
\caption{This is a table}       % A caption for the table
\begin{tabular{ |c|c|c| }       % three columns, each with the text centered in each cell, and lines seperating each column 
 \hline                         % if you want any horizontal lines in your table you call \hline
 cell1 & cell2 & cell3 \\       % each cell is separated with an & and when you are ready to go to the next row you should type \\
 cell4 & cell5 & cell6 \\ 
 cell7 & cell8 & cell9 \\ 
 \hline
\end{tabular}
\label{tab:table_ex}                 
\end{center}
\end{table}
```

This is all you generally need to make basic tables. There are many different ways to construct simple tables, and Overleaf goes over several examples on how to [adjust cell widths, table dimensions, and making multi-tables](https://www.overleaf.com/learn/latex/Tables), but we will not address those things here. The default table size is generally good enough. One option when making tables whihc is very important comes after the `\begin{table}` command. LaTeX will try and judge the best place to put figures and tables. `[h]` tells LaTeX that you want to put the table here and it shouldn't try to optimize the placement of the table. Other options include, but are not limited to: `[t],[b],[p]`, which tell latex to put the table at the top, bottom, or its own page respectively. 

Finally, no table is complete without a caption to explain its contents are. Depending on the journal you are writing for, captions can go at the top or bottom of figures or tables. Gererally, captions go at the tops of tables and the bottom of figures. You can add a caption through the `\caption{}` command.

## Exercise
** Lets make a quick table of thermodyncamic parameters. Try and reproduce the table below. **

![table](/images/Tab-Ex.png) 

The solution can be found [here](soln4.md)

[Creating Figures >>>](figures.md)

[<<< Back](math.md)

[<<< Home](../README.md)
