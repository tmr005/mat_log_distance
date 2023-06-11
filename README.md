# mat_log_distance

## Overview
This repo contains a Jupyter Notebook to adapt the method introduced in Lin, Kong, and Sun (2019) to:
  - simulate a time series of graphs from a given distribution (Sections I & II)
  - simulate a change point in the time series (Section II.D)
  - calculate distances between graphs with a given time series of graph laplacians using matrix logs (Section III.B)
  - detect change points in a time series (Section III.C)
  - implement the above with simulated data (Section IV)
  - dicuss next steps (Section V)

## Motivation
This project was inspired by the work "Using Causal Inference to Explore Government Policy Impact on Computer Usage" by Lechuan Wang and Mingjia Zhu, with advisors Alex Cloninger, Babak Salimi, and Julien Sebot. The end goal (as discussed in Section V) is to detect change points in a time series of transition matrices (from the compute data referenced in this work) using graph laplacians and matrix logs and determine how these change points correspond to events before, during, and after the COVID-19 pandemic.

## Main Reference
Method adapted for calculcating distances time series of matrices:
- Lin, Zhenhua, Dehan Kong, and Qiang Sun. "Modeling Symmetric Positive Definite Matrices with An Application to Functional Brain Connectivity." arXiv preprint arXiv:1907.03385 (2019). https://arxiv.org/pdf/1907.03385.pdf
  - Method in Sections 3.2 and 3.3

## Background Resources
- Harchaoui, Zaid, Eric Moulines, and Francis Bach. "Kernel change-point analysis." Advances in neural information processing systems 21 (2008). https://www.di.ens.fr/~fbach/nips2008_kercha.pdf
- Aminikhanghahi, Samaneh, and Diane J. Cook. "A survey of methods for time series change point detection." Knowledge and information systems 51.2 (2017): 339-367. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5464762/
- Spielman, Daniel A. (draft of) Spectral and Algebraic Graph Theory. http://cs-www.cs.yale.edu/homes/spielman/sagt/sagt.pdf
  - Chapter 1 & 2 "Introduction and Background", Chapter 10 "Random Walks on Graphs"
- Jaffe, Ariel, et al. "Randomized near-neighbor graphs, giant components and applications in data science." Journal of applied probability 57.2 (2020): 458-476. https://www.cambridge.org/core/journals/journal-of-applied-probability/article/randomized-nearneighbor-graphs-giant-components-and-applications-in-data-science/7A3CD4B815489F96B69F63A079037B06 
  - Gal Mishne's paper on nearest neighbor graphs (why use k = N/5 to have fully connected graph)
- https://math.stackexchange.com/questions/705758/power-series-for-a-matrix-inverse
  - Power series for a matrix inverse
- Spielman, Daniel A., and Nikhil Srivastava. "Graph sparsification by effective resistances." Proceedings of the fortieth annual ACM symposium on Theory of computing. 2008. http://www.cs.cornell.edu/~abrahao/tdg/papers/p563.pdf 
  - Asymptotic expansion on I = L * L^-1 -> inverse of laplacian * e
- Lee, John Aldo, and Michel Verleysen. "Nonlinear dimensionality reduction of data manifolds with essential loops." Neurocomputing 67 (2005): 29-53. https://doi.org/10.1016/j.neucom.2004.11.042
  - for potential extensions
