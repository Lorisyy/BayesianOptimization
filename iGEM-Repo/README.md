# Bayesian Optimization Used in Bio-Design
## Reference 
  Nature Communication: [Towards a fully automated algorithm driven platform for biosystems design，2019 Nov 13;10(1):5150. doi: 10.1038/s41467-019-13189-z.](https://pubmed.ncbi.nlm.nih.gov/31723141/)
  
## Introduction
Here we mainly used a key program: Applied_Bayesian_Optimization.ipynb (Also, you may write it as a .py format program).  
1. Gaussian process：
Given an input $x_n$ , we suppose the corresponding \textbf{function value} $f(x_n)$ comes from a Gaussian process, that is, every $\{f(x_n)_{n=1}^{N}\}$ corresponds to Gaussian distribution. The covariance between the two function values $f(\textbf{x})$ and $f(\textbf{x'})$ is kernel function $K(\textbf{x},\textbf{x'})$ which is given in the Python package spearmint.    

So, having a prior assumption of the shape of $f(\textbf{x})$ by Gaussian process, we repeatedly add a new point $(x_n,f(x_n))$ and renew our understanding of $f(\textbf{x})$.

2. Acquisition function:  
The aim of acquisition function is to decide which point $\textbf{x}$ to try next using the existing knowledge of $f(\textbf{x})$. The policy is to choose $x_{next}=argmax_\textbf{x} a(\textbf{x})$, in the other word, the $\textbf{x}$ that maximizes acquisition function $a(\textbf{x})$.  

There are many types of acquisition function, including EI, CI, LCB. We choose EI as our acquisition function, partly because it performs better in preventing the algorithm being trapped around some local extreme point.


### The input :  
1. **Initial Experimental result** using given fixed-dimensional (1-5, normally) initial independent variables.  
2. **Number of iterations**,  this depends on how many times are you willing to try to get a relatively optimal solution.   
3. **Experimental result every iteration round** using possible global optimal coefficients so far, input the result corresponding to those coefs.  
### The Output :
1. **Current global optimal solution** after every iteration round.
2. **Global optimal solution** among the whole experiments you did so far.

## Dependency
  [Numpy](https://numpy.org)  
  [Bayesian-Optimization](https://pypi.org/project/bayesian-optimization/)   
  [SciPy](https://www.scipy.org)   
  [scikit-learn==0.22.x](https://scikit-learn.org/0.22/)
