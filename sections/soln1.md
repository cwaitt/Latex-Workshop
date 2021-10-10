# The Preamble Example

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

\usepackage{graphicx}                          % This package will allow use to make and refer to figures
\graphicspath{ {./images/} }                   % that exist in the images folder


%%% Document specific things %%%

\title{Hello World}                            % The title of your project            
\author{Craig Waitt}                           % Author name
\date{October 2021}                            % The date

```

We add the graphicx package through `\usepackage{graphicx}` command and we add a second line of code that tell LaTeX where to look for the images and figures we will include later. The location (or path) of the figures is set by `\graphicspath{ {./images/} }` and by adding an 'images' folder in the workspace on the left. Feel free to use any name for the folder you find appropriate.

[<<< Back](preamble-body.md)

