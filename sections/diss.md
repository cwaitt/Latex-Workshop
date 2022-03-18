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
