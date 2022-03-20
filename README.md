# classifiers
A project where different classifier algorithms are tested. The following algorithms are covered in this project.
#### K-nearest neighbours
Classified cases based on the neghbours
1. Pick value of K
2. Calculate distance of unknown case from all cases
3. Find K nearest neighbours
4. Predict response  = most popular among neighbours
Choosing right K is the modelling <br>
Can also be used for regression: as median of neighbours

#### Decision trees
Built by splitting training set into distinct nodes.  <br>
1. Choose attribute : the one that best splits the data (label) or purity of the leaves
2. Calculate significance of the attribute 
3. Split data based on best attributes 
4. Go to step 1

Entropy =  $-P(a)\log P(a)-P(b)\log P(b)$: amount of randomness<br>
Information gain = Entropy before split - weighted entropy after split, (weighted by the size of the child nodes) <br>
The decision tree algorithm tries to maximise the information gain at each decision node.

#### Logistic regression
Logistic regression is similar to linear regression except that it predicts a _discrete_ value. In fact, mathematically logistic regression returns a continous valued function in (0,1) which is then mapped to either 0 or 1 if it is below or above a threshold value (usually 0.5). Logistic regression can be considered as a classifier which predicts the probability to be in a particular class.

Linear regression has the functional form, $y=\theta_0+\theta_1x_1+\theta_2x_2+\ldots$, and the model finds the values of $\theta_i$ that best fits the data. Logistic regression requires a function with a range (0,1).

Sigmoid function is one such function which has the form $\sigma(x)=e^x/1+e^x$. Using sigmoid function, a model can be used to fit the data using,
$$P(y=1)=\frac{e^{\Theta^TX}}{1+e^{\Theta^TX}},$$
where $\Theta=\left(\theta_0,\theta_1,\ldots\right)$ and $X=\left(x_1,x_2,\ldots\right)$.

#### Support vector machines
A supervised algorithm that can classify based on a separator. It uses a hyperplane in a higher dimensional space to separate the classes. The mathematical function which maps data to the higher dimensional space - Kernelling (Can be linear, polynomial, sigmoid, radial basis function). Goal is to choose a hyperplane with as big a margin (support vectors) as possible. This is an optimization problem.

##### Evaluation metrics
Jaccard Index : size of the intersection/size of the union of labels <br>
F1-score (confusion matrix) : Precision, recall, f1 score is harmonic mean of P and R <br>
Log loss : when the predicted output is a probability value (smaller the better)
