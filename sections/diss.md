# Notre Dame Dissertation Template

The University of Notre Dame has gathered a number of resources useful to dissertation and thesis authors [here](https://graduateschool.nd.edu/policies-forms/doctoral-dissertations-masters-theses/author-resources/). There are two tools provided by the university to get you started writing your dissertation: an Microsoft word template and a Latex class file. To those who are new to Latex, the initial directions may seem daunting or overwhelming. However, the university has integrated this Latex class package into Overleaf, making dissertationa and thesis writing much more simple. This page will walk through the steps needed to create your document, and create a template that you can begin writing in.

**Note:** This tutorial was written in 2022, and the Latex package was created in 2013. Since it inception, not much has changed in the document formating requirements. However, the graduate school may change how they want the documents to be formatted. You should always follow the directions presented by the graduate school. In the event the graduate school does change their formatting requirements, and you still wish to use Latex to write your document, please reach out to the graduate school for assistance at dteditor@nd.edu. You can also find the original source code and examples on how to write your document in Latex [here](https://github.com/ndlib/nddiss)

## Learning Objectives

1. What is **nddiss2e** and how to customize the options to format the dissertation or thesis.

2. How to set up the preamble.

3. How to create chapters and sections.

4. Cover advanced topics you may (or may not need)

## The **nddiss2e** package

The **nddiss2e** package was written using a subset of preexisting packages and customized functions to make formating you document easier. However, that also means that you may find issues was adding your own packages to your Latex document. For example, if you have a set of subfigures that you would like to caption individually, one would use the `\usepackage{subcaption}` package, however, there are conflicts between this package and the nddiss2e package that prevent both from working correctly. If you would like to use additional packages you will either need to find your own work around, or download the source code, modify it, and run it on your personal computer (meaning you can't use Overleaf). Fortunatly, most dissertations or theses don't require the use of such exotic packages and there for you should be fine.

Lets start by creating a new file in Overleaf, and adding the following lines in your document:

```
\documentclass[]{nddiss2e}

% Titles may be 1-4 lines long. If your title is longer than 4 lines,
% the class file may have difficulty formatting the title page.
% Line-breaks in the title have to be protected with `\protect`.
\title{My Dissertation Title: A very long winded and \protect\\ professional looking title that only a select few \protect\\ people will end up reading!!}
\author{My Name}
\work{Dissertation} % or \work{Thesis}
%\degaward{Doctor of Philosophy} % or 
\degaward{Master of Science \\ in \\ Subject}
\advisor{Advisor Name}
%\secondadvisor{Gordon Gray} % if you have two advisers are using the option twoadvisors
\department{Department}

\begin{document}

\frontmatter % All the items before the first chapter go in ``frontmatter''

\maketitle

\end{document}

```

When you compile this document, you should see 2 pages corresponding to the coverpage of your document. The first page should not be submitted with your dissertation, and the second should look more professional. The **nddiss2e** class has preloaded a set of commonly used packages such as asmath, and graphicx, etc. You may add other packages as needed, but other than the author and document information, the `\documentclass[]{nddiss2e} is the one and only line needed in the preamble. The open `[]` are there to customize some options which we will cover momentarily.

The other lines in the preamble set up the document title, author name, and some other things that are needed. Edit the information in the `{}` brackets to reflect what your dissertation or thesis will cover. If you need a second advisor, leave that commented out for the time being. If you have a long title that spans mulitple lines, use the ``\protect\\` command. This will force a line break in the Title. The `\protect` just forces the line break to occur and is only needed in the title. 

All of this information gets transfered to the \maketitle command, which appears between the `\begin{document}` and `\end{document}` commands. The command `\frontmatter` is need to let Latex know which pages should be numbered with arabic or roman numerals. All the thing proceeding the physical dissertation, such as the abstract and table of contents, should have roman numerals and the chapters should have arabic numerals.

## Customize the **nddiss2e** options 

Even though we didnt specify any options in the `[]`, some default values were assumed. These are the options availible to use:

1. Whether or not you are writing a draft, a document to be reviewed, or the final document (`draft`, `review`, or `final`)
2. Whether you want the citations to be sorted numerically how they appear or by author-date (`numrefs` or `textrefs`)
3. Whether you need a second advisors signature (add the option `twoadvisors`)
4. Whether or not you want the nddiss2e info to show up, which it shouldn't when you submit your thesis (`noinfo`)
5. How you want the citations to be presented in the document (`sort`, `compress`, or `sort&compress`)

Update the **nddiss2e** line with the following options:

```
\documentclass[final,numrefs,sort&compress,noinfo]{nddiss2e}
```

You will notice a few warning in your log file. You can ignore these files. They are warning you of conflicts within some internally used packages however these should have little impact on our final project. You are now set to start writing your document.

## Frontmatter

In this section we will cover some of the things that one adds to their dissertation or document before getting into the meat of the content. These thing follow the `\maketitle` command.

### Copyright

You must either set the copyright information or put your work in the public domain.

```
\copyrightholder{Advisor Name} % See template or documentation for
\copyrightyear{2022}           % other copyright options.
\copyrightlicense{CC-BY-4.0}
\makecopyright
```

### Abstract

Abstracts are required for dissertations but optional for masters theses.

```
\begin{abstract}
	Abstract content goes here. It can run over a page if needed. I am only indenting to help readablilty you don't need to indent.
\end{abstract}
```

### Dedication

Dedications are optional.

```
\renewcommand{\dedicationname}{NEW DEDICATION NAME}

\begin{dedication}
	I would like to thank ...
\end{dedication}
```

### Table of Contents

These are required. You do not need to physically add the Figure and Table numbers and pages to this section. Latex will take care of that for you. We only need to initialize the page and tell latex what we want ordered first, the figures or the tables.

```
\tableofcontents
\listoffigures
\listoftables
```

### Preface

A preface is optional.

```
\begin{preface}
	I would like to preface this work ...
\end{preface}
```

### Acknowlegements

```
\begin{acknowledge}
 I would like to thank ...
\end{acknowledge}
```

### Symbols

Symbols section is optional

```
\begin{symbols}
  \sym{\mathcal{F}}{sighting frequency of Gnus about campus}
\end{symbols}
```

The whole document with the preamble and frontmatter should look something like this.

```
\documentclass[final,numrefs,sort&compress,noinfo]{nddiss2e}

% Titles may be 1-4 lines long. If your title is longer than 4 lines,
% the class file may have difficulty formatting the title page.
% Line-breaks in the title have to be protected with `\protect`.
\title{My Dissertation Title: A very long winded and \protect\\ professional looking title that only a select few \protect\\ people will end up reading!!}
\author{My Name}
\work{Dissertation} % or \work{Thesis}
%\degaward{Doctor of Philosophy} % or 
\degaward{Master of Science \\ in \\ Subject}
\advisor{Advisor Name}
%\secondadvisor{Gordon Gray} % if you have two advisers are using the option twoadvisors
\department{Department}

\begin{document}

\frontmatter % All the items before the first chapter go in ``frontmatter''

\maketitle

\copyrightholder{Advisor Name} % See template or documentation for
\copyrightyear{2022}           % other copyright options.
\copyrightlicense{CC-BY-4.0}
\makecopyright

\begin{abstract}
	Abstract content goes here. It can run over a page if needed. I am only indenting to help readability you don't need to indent.
\end{abstract}

\renewcommand{\dedicationname}{NEW DEDICATION NAME}

\begin{dedication}
	I would like to thank ...
\end{dedication}

\tableofcontents
\listoffigures
\listoftables

\begin{preface}
	I would like to preface this work ...
\end{preface}

\begin{acknowledge}
 I would like to thank ...
\end{acknowledge}

\begin{symbols}
  \sym{\mathcal{F}}{sighting frequency of Gnus about campus}
\end{symbols}

\end{document}

```

## Mainmatter

The mainmatter is the content of your dissertation or thesis. This is where you begin your chapters and sections.

### Unumbered Chapters

If you need an unnumbered chapter for some reason, you can initilize it with the `\unnumchapter{} command` followed by the content under the chapter heading.

```
\unnumchapter{Making Unnumbered Chapters}
	You should not have more than 1 of these before your first chapter however there is nothing preventing you from making more. 
```

### Chapters

We have been editing all of this information in the file **main.tex**, you can continue to write your entire document in this file, but you may find it becoming to large to handle. Additionally, if you decide to reorder your chapters, you may find it difficult to copy and past things around. Therefore it is recommended to create new chapters in the workspace and use the `\include{}` command to integrate them into your document.

First, lets create a new file called **chapter1.tex**, and add the following information to that file:

```
\chapter{Introduction}

\section{Overview}

This is a high-level overview of what is expected in this chapter.

\subsection{Background}
Here is some background information. \footnote{And I'll include a footnote for fun.}

% % uncomment the following lines,
% if using chapter-wise bibliography
%
% \bibliographystyle{ndnatbib}
% \bibliography{example}
```

Next, go back to **main.tex** and add:

```
\mainmatter

\include{chapter1.tex}
```

If you recompile the PDF, the content for chapter 1 will be imported into **main.tex**, and the Table of Contents will update with the location of Figures and Tables as they are added. If using chapterwise biblography, uncomment the last two lines and the bibliography will be displayted (if you have imported a **example.bib** file like the one presented in the [citation section](./citations.md) of the Latex Workshop). You can add successive chapters this way, which keeps your workspace manageble. 

### Appendix

You can also add an appendix after you have imported your chapters by using the `\appendix` command, followed by `\include{appendix.tex}` if you have created an appendix file.

So far, the template of **mian.tex** should look something like this:

```
\documentclass[final,numrefs,sort&compress,noinfo]{nddiss2e}

% Titles may be 1-4 lines long. If your title is longer than 4 lines,
% the class file may have difficulty formatting the title page.
% Line-breaks in the title have to be protected with `\protect`.
\title{My Dissertation Title: A very long winded and \protect\\ professional looking title that only a select few \protect\\ people will end up reading!!}
\author{My Name}
\work{Dissertation} % or \work{Thesis}
%\degaward{Doctor of Philosophy} % or 
\degaward{Master of Science \\ in \\ Subject}
\advisor{Advisor Name}
%\secondadvisor{Gordon Gray} % if you have two advisers are using the option twoadvisors
\department{Department}

\begin{document}

\frontmatter % All the items before the first chapter go in ``frontmatter''

\maketitle

\copyrightholder{Advisor Name} % See template or documentation for
\copyrightyear{2022}           % other copyright options.
\copyrightlicense{CC-BY-4.0}
\makecopyright

\begin{abstract}
	Abstract content goes here. It can run over a page if needed. I am only indenting to help readability you don't need to indent.
\end{abstract}

\renewcommand{\dedicationname}{NEW DEDICATION NAME}

\begin{dedication}
	I would like to thank ...
\end{dedication}

\tableofcontents
\listoffigures
\listoftables

\begin{preface}
	I would like to preface this work ...
\end{preface}

\begin{acknowledge}
 I would like to thank ...
\end{acknowledge}

\begin{symbols}
  \sym{\mathcal{F}}{some symbols}
\end{symbols}

\mainmatter

\include{chapter1.tex}

\end{document}

```

## Backmatter

Finally, we have the backmatter, which includes all the bibliography information if you are not doing it chapter-wise. You can also enter the bibliography manually by using the bibitem manually, but that is not recommended. If you are using Zotero or Mendeley, click the upload button and import the citations. Otherwise create a file that ends in **.bib** to store your citations.

```
\backmatter

\bibliographystyle{abbrvnat} % The standard abbrvnat style should be acceptable. Also provided with both the advanced and standard
\bibliography{example}
```

We have note cited anything yet but you should see a bibliography page that is empty and the table of contents should be updated.

With that, we have structured the template for you to write your dissertation or thesis.

```
\documentclass[final,numrefs,sort&compress,noinfo]{nddiss2e}

% Titles may be 1-4 lines long. If your title is longer than 4 lines,
% the class file may have difficulty formatting the title page.
% Line-breaks in the title have to be protected with `\protect`.
\title{My Dissertation Title: A very long winded and \protect\\ professional looking title that only a select few \protect\\ people will end up reading!!}
\author{My Name}
\work{Dissertation} % or \work{Thesis}
%\degaward{Doctor of Philosophy} % or 
\degaward{Master of Science \\ in \\ Subject}
\advisor{Advisor Name}
%\secondadvisor{Gordon Gray} % if you have two ##advisers are using the option twoadvisors
\department{Department}

\begin{document}

\frontmatter % All the items before the first chapter go in ``frontmatter''

\maketitle

\copyrightholder{Advisor Name} % See template or documentation for
\copyrightyear{2022}           % other copyright options.
\copyrightlicense{CC-BY-4.0}
\makecopyright

\begin{abstract}
	Abstract content goes here. It can run over a page if needed. I am only indenting to help readability you don't need to indent.
\end{abstract}

\renewcommand{\dedicationname}{NEW DEDICATION NAME}

\begin{dedication}
	I would like to thank ...
\end{dedication}

\tableofcontents
\listoffigures
\listoftables

\begin{preface}
	I would like to preface this work ...
\end{preface}

\begin{acknowledge}
 I would like to thank ...
\end{acknowledge}

\begin{symbols}
  \sym{\mathcal{F}}{some symbols}
\end{symbols}

\mainmatter

\include{chapter1.tex}

\backmatter

\bibliographystyle{abbrvnat} % The standard abbrvnat style should be acceptable. Also provided with both the advanced and standard
\bibliography{example}

\end{document}

```

The rest of the document is all content based and requires the basic Latex Commands presented earlier in this workshop. In the final section, we will cover some advanced formating option that were not previously covered. Please remember to follow the formating directions provided by the graduate school. 

## Advanced Typsetting

### Extended/Long Tables

Be aware that page-spanning tables a Very Odd Creatures. The "longtable" environment in LaTeX does some deep Voodoo to make everything work out properly. One of its deep incantations is to make the table appear as though it is double spaced.  You can fix this by trailing each line with "\\[-6em]" instead of just "\\". When using longtable it is also important to compile your file more than once.

```
\begin{center}
  \begin{longtable}{lccccc}
    \caption{Electoral College Results for the \NoCaseChange{LoG} Election in the Year
2000\label{tbl:votes}\/}\\
        \toprule
        Candidate\footnote{note all names begin with G} & Anti-management & Cuteness & Friendliness & Furriness & Aggregate \\
        \midrule
\endfirsthead % Everything above goes at the top of the 1st page only
% As with the first header, we don't want obscene amounts of space for
% subsequent headings either, and eliminate an em of whitespace.
  \caption[]{{\em Continued}}\\
  \midrule
  Candidate & Anti-management & Cuteness & Friendliness & Furriness & Aggregate \\
  \midrule
\endhead % Everything above here (and below the \endfirsthead) goes at the top
         % of continuation pages.  The [] argument prevents a duplicate
         % entry from appearing in the table of contents.
% The following 3 lines are provided as an example only -- per ND
% guidelines, the footer at the bottom of a page for a longtable
% should not have a bottom line.  Only the absolute bottom of the
% table should have a final \bottomline

%  \midline
%  \multicolumn{6}{|r|}{\textit{continued}\ldots} \\
%  \bottomrule
\endfoot % The above section goes at the bottom of continuation pages
  \bottomrule
\endlastfoot % The very last bottom of the table
    Glen & 6.2 & 7.0 & 6.1 & 9.8 & 7.2 \\
    Goober & 6.9 & 2.1 & 5.7 & 4.1 & 4.6 \\
    Genevra & 2.2 & 2.0 & 1.1 & 1.1 & 1.6 \\
    Greg & 8.3 & 0.4 & 1.1 & 9.5 & 4.8 \\
    Gina & 6.0 & 7.8 & 6.4 & 4.9 & 6.2 \\
    Geof & 1.1 & 8.7 & 3.7 & 7.3 & 5.2 \\
    Grendel & 2.8 & 1.7 & 3.4 & 3.2 & 2.7 \\
    Geronimo & 1.2 & 1.2 & 8.8 & 2.2 & 3.3 \\
    Gabrielle & 4.7 & 3.6 & 0.8 & 2.0 & 2.7 \\
    Giovani & 8.4 & 5.8 & 3.4 & 7.4 & 6.2 \\
    Graham & 4.7 & 5.8 & 5.3 & 0 & 3.9 \\
    Gil & 5.9 & 4.0 & 5.5 & 7.6 & 5.7 \\
    Gerald & 2.0 & 3.7 & 8.0 & 4.3 & 4.5 \\
    Guilani & 7.7 & 3.9 & 2.7 & 6.4 & 5.1 \\
    Guido & 7.6 & 4.3 & 6.5 & 1.0 & 4.8 \\
    Godzilla & 5.1 & 2.2 & 5.3 & 6.9 & 4.8 \\
    Gail & 5.7 & 7.9 & 4.1 & 1.0 & 4.6 \\
    Garth & 4.7 & 7.1 & 2.5 & 3.0 & 4.3 \\
    Gavin & 1.1 & 9.5 & 0.4 & 8.0 & 4.7 \\
    George & 9.5 & 4.5 & 9.1 & 7.5 & 7.6 \\
    Gunnar & 1.4 & 5.8 & 4.8 & 6.2 & 4.5 \\
    Gillian & 7.6 & 9.0 & 6.4 & 4.6 & 6.9 \\
    Greta & 1.5 & 0.5 & 0.9 & 7.7 & 2.6 \\
    Gabby & 1.2 & 3.3 & 7.0 & 2.1 & 3.4 \\
    Gaetena & 6.8 & 1.9 & 4.1 & 8.3 & 5.2 \\
    Ganet & 2.3 & 1.1 & 8.5 & 7.3 & 4.8 \\
    Gardenia & 1.8 & 9.5 & 9.9 & 3.0 & 6.0 \\
    Genna & 5.2 & 3.7 & 3.4 & 3.8 & 4.0 \\
    Genesis & 1.7 & 8.3 & 6.7 & 4.9 & 5.4 \\
    Genaveve & 4.7 & 8.9 & 3.4 & 9.2 & 6.5 \\
    Gene & 3.3 & 6.9 & 0.6 & 5.5 & 4.0 \\
    Gilda & 5.2 & 4.6 & 9.9 & 1.4 & 5.2 \\
    Goldie & 8.9 & 9.1 & 2.0 & 8.2 & 7.0 \\
    Grace & 5.9 & 3.2 & 3.1 & 4.3 & 4.1 \\
    Gretchen & 4.5 & 6.5 & 1.6 & 1.3 & 3.4 \\
    Garrick & 4.8 & 5.7 & 9.4 & 5.1 & 6.2 \\
    Gallagher & 7.4 & 0.4 & 7.6 & 0.4 & 3.9 \\
    Gerry & 1.4 & 8.8 & 4.7 & 0.5 & 3.8 \\
    Gertrude & 9.1 & 8.3 & 0.4 & 5.5 & 5.8 \\
    Gehosephet & 6.6 & 2.9 & 8.3 & 4.4 & 5.5 \\
    Gohn & 8.7 & 2.6 & 7.4 & 2.3 & 5.2 \\
    Gibby & 8.7 & 6.9 & 4.7 & 7.2 & 6.9 \\
  \end{longtable}
\end{center}
```
