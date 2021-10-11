# Cropping Figures

```
\subsection{Example}
\begin{figure}
    \centering
    \includegraphics[scale=0.15, trim={0cm 0cm 0cm 0cm},clip]{"./cosmic.jpg"}
    \caption{This image is not cropped.}
    \label{fig:cosmic}
\end{figure}

\begin{figure}
    \centering
    \includegraphics[scale=0.15, trim={0cm 0cm 40cm 0cm},clip]{"./cosmic.jpg"}
    \caption{This image is not cropped.}
    \label{fig:cosmic}
\end{figure}
```

The trim command is essentially the same thing as crop. The numbers in trim refer to the left, bottom, right, and top sections of the image respectively. I also included a unit of cm to make cropping easier (for me). 

[<<< Back](figures.md)
