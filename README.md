# Supervised-ML-Library-Implementation

**How to download this project and dependencies:**
 1. Install Anaconda/Jupyter Notebook
 2. Install all dependencies/libraries as stated later
 3. Download all the given files and put them in a folder named “X” on the desktop
 4. open Anaconda Prompt and type <jupyter notebook>
 5. Desktop -> X -> Linear Regression
 6. Run the ipynb file

**Aim:**
In this project I have implemented algorithms such as normal equations, gradient descent, stochastic gradient descent, lasso regression and ridge regression from scratch and done linear as well as polynomial regression analysis on a 1338*4 dimension dataset which is available in the folder dataset.

**Code Design**

**Key points to ponder upon:**

**Q. While generating matured features (polynomial features in this case), is it better to:
A) generate the matured (polynomial) features from the given features and then scale those obtained matured features 
                        OR
B) first scale the given features and then generate matured (polynomial) features from those scaled features.**

A.If you first scale down, your values usually lie between 0, 1 (normalise). Now if you generate matured features like x^20 (basically any high degree polynomial), those values become too small and almost become 0 in the standard precision of your PC. But if you generate the features and then scale, those very high values which were generated will now be scaled into (0,1). Values will be considerable to work with. So I recommend you all guys do this.

**Q.Why can't we think of lambda (regularisation parameter) as a trainable parameter instead of a hyperparameter and learn it as well during GD/SGD? Let's assume we are dealing with L2 regularisation (ridge) with initial lambda value as 0.5.What I am asking is why can't lambda be learnt like the other Weights**

A.The thing is is L is the L2 loss function, dL/d lambda will be sum of norms of W, which is always a positive value. Now this will cause the gradient descent to always pull the value of lambda down to 0 and later negative.So now if lambda is negative, you favour larger weights as you can see that the Loss term will decrease with larger weights. This beats the point of regularisation

**Teammembers:**

Rishabh Nahar 
Samkit Jain
