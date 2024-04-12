# Working Paper Model

WorkingPaperModel is a LaTeX template for working papers designed by Fabien Petit.

---------------------

FILES are organized as follows:
    main.tex : main file that determines: packages, packages options, meta-data and structure of the paper
    references.bib : bibliography

DIRECTORIES are organized as follows:
    - _chapter: content of the paper. Organized at the section level.
    - _deprecated: contains all deprecated parts of the paper.
    - _graphic: contains all graphics. The figure environment is defined in the content.
    - _logo: contains all logos for presentations.
    - _slide: content of the presentation.
    - _tabular: contains all tabulars. The table environment is defined in the content.

---------------------

LABELS and REFERENCES have the following pattern:
    - for SECTIONS: the name of the section with 'sec:' before
        - example: \label{sec:introduction} \ref{sec:introduction}
    - for EQUATIONS: the name of the equation with 'eq:' before
        - example: \label{eq:utility} \eqref{eq:utility}
    - for FIGURES: the name of the figure with 'fig:' before
        - example: \label{fig:gdp-growth} \ref{fig:gdp-growth}
    - for TABLES: the name of the table with 'tab:' before
        - example: \label{tab:parameters} \ref{tab:parameters}

---------------------

STANDARD FIGURE ENVIRONMENT :

```latex
\begin{figure}[!t]
    \centering
    \caption{Title}
    \includegraphics[width=\textwidth]{_graphic/graph.jpg}
    \label{fig:label}
    \vspace{-3em}
    \justify\singlespacing\scriptsize\textit{Notes}: Notes here.
\end{figure}
```

STANDARD TABLE ENVIRONMENT :

```latex
\begin{table}[!t]
    \centering
    \caption{Title}
    \label{tab:label}
    % \resizebox*{\textwidth}{!}{
    \begin{threeparttable}
        % \setlength{\tabcolsep}{6pt}
        % \small
        \input{_tabular/table}
        \begin{tablenotes}[flushleft]
            \scriptsize{\item \textit{Notes}: Notes here}
        \end{tablenotes}
    \end{threeparttable}
    % }
\end{table}
```