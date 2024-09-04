\documentclass{article}
\usepackage{listings}
\usepackage{hyperref}

\title{Protein-Protein Link Prediction}
\author{}
\date{}

\begin{document}

\maketitle

This project implements the Neural Common Neighbour with Completion (NCNC) algorithm for link prediction using GraphSage. The NCNC algorithm is based on the research paper titled \emph{Neural Common Neighbour with Completion for Link Prediction}, and it extends the GraphSage framework for more accurate link prediction in graph data.

\section*{Files}

\begin{itemize}
  \item \texttt{NeighbourOverlap.py}: Python script implementing the neural common neighbour with completion for link prediction.
  \item \texttt{model.py}: Contains the implementation of the GraphSage model.
  \item \texttt{utils.py}: Utility functions used in the project.
  \item \texttt{ogbdataset.py}: Helper functions for loading datasets from the Open Graph Benchmark (OGB).
\end{itemize}

\section*{Datasets}

The project supports three datasets for link prediction:

\begin{itemize}
  \item Cora
  \item Citeseer
  \item Pubmed
\end{itemize}

\section*{Running the Code}

To reproduce the results on the datasets, run the following commands:

\subsection*{Cora Dataset}

\begin{lstlisting}
!python NeighborOverlap.py --xdp 0.7 --tdp 0.3 --pt 0.75 --gnnedp 0.0 --preedp 0.4 --predp 0.05 --gnndp 0.05 --probscale 4.3 --proboffset 2.8 --alpha 1.0 --gnnlr 0.0043 --prelr 0.0024 --batch_size 1152 --ln --lnnn --predictor cn0 --dataset Cora --epochs 100 --runs 10 --model puregcn --hiddim 256 --mplayers 3 --testbs 8192 --maskinput --jk --use_xlin --tailact
\end{lstlisting}

\subsection*{Citeseer Dataset}

\begin{lstlisting}
!python NeighborOverlap.py --xdp 0.7 --tdp 0.3 --pt 0.75 --gnnedp 0.0 --preedp 0.4 --predp 0.05 --gnndp 0.05 --probscale 4.3 --proboffset 2.8 --alpha 1.0 --gnnlr 0.0043 --prelr 0.0024 --batch_size 1152 --ln --lnnn --predictor cn0 --dataset Citeseer --epochs 100 --runs 10 --model puregcn --hiddim 256 --mplayers 3 --testbs 8192 --maskinput --jk --use_xlin --tailact
\end{lstlisting}

\subsection*{Pubmed Dataset}

\begin{lstlisting}
!python NeighborOverlap.py --xdp 0.7 --tdp 0.3 --pt 0.75 --gnnedp 0.0 --preedp 0.4 --predp 0.05 --gnndp 0.05 --probscale 4.3 --proboffset 2.8 --alpha 1.0 --gnnlr 0.0043 --prelr 0.0024 --batch_size 1152 --ln --lnnn --predictor cn0 --dataset Pubmed --epochs 100 --runs 10 --model puregcn --hiddim 256 --mplayers 3 --testbs 8192 --maskinput --jk --use_xlin --tailact
\end{lstlisting}

Feel free to adjust the parameters as needed.

\section*{Reference}

\begin{quote}
@article{wang2023neural,  
  title={Neural common neighbor with completion for link prediction},  
  author={Wang, Xiyuan and Yang, Haotong and Zhang, Muhan},  
  journal={arXiv preprint arXiv:2302.00890},  
  year={2023}
}
\end{quote}

\end{document}
