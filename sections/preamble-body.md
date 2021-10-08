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

# The Body
