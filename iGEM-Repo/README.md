# Bayesian Optimization Used in Bio-Design
## Reference 
  Nature Communication: [Towards a fully automated algorithm driven platform for biosystems design，2019 Nov 13;10(1):5150. doi: 10.1038/s41467-019-13189-z.](https://pubmed.ncbi.nlm.nih.gov/31723141/)
  
## Introduction
Here we mainly used a key program: Applied_Bayesian_Optimization.ipynb (Also, you may write it as a .py format program).

### The input :  
1. **Initial Experimental result** using given fixed-dimensional (1-5, normally) initial independent variables.  
2. **Number of iterations**, this depends on how many vc are you willing to spend to get a relatively optimal solution.  
3. **Experimental result every iteration round** using possible global optimal coefficients so far, input the result corresponding to those coefs.  
### The Output :
1. **Current global optimal solution** after every iteration round.
2. **Global optimal solution** among the whole experiments you did so far.

## Dependency
  [Numpy](https://numpy.org)  
  [Bayesian-Optimization](https://pypi.org/project/bayesian-optimization/)   
  [SciPy](https://www.scipy.org)   
