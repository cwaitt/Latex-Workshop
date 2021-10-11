# Making Figures

Like tables, inserting figures can be somewhat tediuos, but in my opinion is much easier the Microsoft Word (or related products). Before we begin, we will need to add some figures to our folder to use in our LaTeX document. On the GitHub page, I have included a folder called [examples/inserting_figures](/examples/inserting_figures). Dowload the images onto your local machine, and upload them to the 'images' folder on your LaTeX project manager.

## Inserting Figures
Similar to tables, LaTeX will try to put the figure where it thinks it should go, so we will overridde LaTeX's "thinking" and force it to a specific location with the `[h]` option. Simply put, when you are ready to add a figure you simply would type:

```
\section{Figures}

To add Figure \ref{fig:overleaf} to your document, you only need to type \textbackslash includegraphics\{\} and then the path to the graphic.

\begin{figure}[h]
    \centering
    \includegraphics{"./overleaf_og_logo.png"}
    \caption{This is the overleaf logo.}
    \label{fig:overleaf}
\end{figure}
```

When you copy this code into your LaTeX code, and recompile the pdf, you should see the Figure with its caption below it. You will also see that we used the command `\ref{fig:overleaf}` before we actually inserted our figure. LaTeX is able to make internal document links in out of order from when they are called.

## Formating Figure

After inserting the image, there are a host of different things you can do, such as crop, resize, and rotating your image. You can also make a single figure which is a composite of multiple figures, but we will not address that in this tutorial. You can learn all about the figure utilities [here](https://www.overleaf.com/learn/latex/Inserting_Images).

### Figure Size

Formating the figure size is pretty simple. After the `\includegraphics{}` command we can specify our options. When resizing a figure. It is important to scale the image uniformally, but there are ways to scale the [width and length separatly](https://www.overleaf.com/learn/latex/Inserting_Images#Changing_the_image_size_and_rotating_the_picture). 

```
\begin{figure}[h]
    \centering
    \includegraphics[scale=2]{"./overleaf_og_logo.png"} % doubles the size of the image
    \caption{This logo is doubled in size.}
    \label{fig:overleaf-2}
\end{figure}

\begin{figure}[h]
    \centering
    \includegraphics[width=\textwidth]{"./overleaf_og_logo.png"}
    \caption{This logo fills the width of the page.}
    \label{fig:overleaf-3}
\end{figure}

Figure \ref{fig:overleaf-2} is doubled in size and Figure \ref{fig:overleaf-3} fills the width of the page. You may notice a button next to the Compile button that has a yellow number. This is a warning telling you there is a better way to code up some piece of LaTeX, you can ignore these warnings. 
```

## Examples 
**Add the cosmic or flower png, scale the image size so it fits on the page, and crop the image so that about half of the image is gone. The solution can be found [here](soln5.md). You can use this [stack exchange](https://tex.stackexchange.com/questions/57418/crop-an-inserted-image) comment for help if you need it.**

[Making Citations >>>](citations.md)

[<<< Back](tables.md)

[<<< Home](../README.md)



