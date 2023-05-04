Download Link: https://assignmentchef.com/product/solved-cs584-assignment-5-use-the-multi-layer-perceptron-algorithm-to-classify-spectralcluster
<br>
Question 1 (40 points)

The SpiralWithCluster.csv contains four variables.

<table width="0">

 <tbody>

  <tr>

   <td width="120"><strong>Name </strong></td>

   <td width="160"><strong>Description </strong></td>

   <td width="140"><strong>Measurement Level </strong></td>

   <td width="140"><strong>Role </strong></td>

  </tr>

  <tr>

   <td width="120">Id</td>

   <td width="160">Case Identifier</td>

   <td width="140">Nominal</td>

   <td width="140">Identifier</td>

  </tr>

  <tr>

   <td width="120">X</td>

   <td width="160">x-coordinate</td>

   <td width="140">Interval</td>

   <td width="140">Feature</td>

  </tr>

  <tr>

   <td width="120">Y</td>

   <td width="160">y-coordinate</td>

   <td width="140">Interval</td>

   <td width="140">Feature</td>

  </tr>

  <tr>

   <td width="120">SpectralCluster</td>

   <td width="160">Cluster Identifier</td>

   <td width="140">Binary</td>

   <td width="140">Target</td>

  </tr>

 </tbody>

</table>




You are asked to use the Multi-Layer Perceptron (MLP) algorithm to classify SpectralCluster.  You will use the sklearn.neural_network.MLPClassifier function with the following specifications.

<ol>

 <li>Each hidden layer will have the same number of neurons</li>

 <li>The initial learning rate is 0.1</li>

 <li>The maximum number of iterations is 5000</li>

 <li>The random seed is 20200408</li>

 <li>The solver for weight optimization is lbfgs</li>

</ol>

Please answer the following questions based on your model.

a. What percent of the observations have SpectralCluster equals to 1? Ans: 50.0 percent of the observation have SpectralCluster equals to 1

b. You will search for the neural network that yields the lowest loss value and the lowest misclassification rate. You will use your answer in (a) as the threshold for classifying an observation into SpectralCluster = 1. Your search will be done over a grid that is formed by cross-combining the following attributes: (1) activation function: identity, logistic, relu, and tanh; (2) number of hidden layers: 1, 2, 3, 4, and 5; and (3) number of neurons: 1 to 10 by 1.  List your optimal neural network for each activation function in a table.  Your table will have four rows, one for each activation function.  Your table will have six columns: (1) activation function, (2) number of layers, (3) number of neurons per layer, (4) number of iterations performed, (5) the loss value, and (6) the misclassification rate.

c. What is the activation function for the output layer?

d.  Which activation function, number of layers, and number of neurons per layer give the lowest loss and the lowest misclassification rate? What are the loss and the misclassification rate? How many iterations are performed?

e. Please plot the y-coordinate against the x-coordinate in a scatterplot. Please color-code the points using the predicted SpectralCluster (0 = Red and 1 = Blue) from the optimal MLP in (d).  To obtain the full credits, you should properly label the axes, the legend, and the chart title.  Also, grid lines should be added to the axes.

f. What is the count, the mean and the standard deviation of the predicted probability Prob(SpectralCluster = 1) from the optimal MLP in (d) by value of the SpectralCluster? Please give your answers up to the 10 decimal places.

Question 2 (60 points)

The SpiralWithCluster.csv contains four variables.

<table width="0">

 <tbody>

  <tr>

   <td width="120"><strong>Name </strong></td>

   <td width="160"><strong>Description </strong></td>

   <td width="140"><strong>Measurement Level </strong></td>

   <td width="140"><strong>Role </strong></td>

  </tr>

  <tr>

   <td width="120">Id</td>

   <td width="160">Case Identifier</td>

   <td width="140">Nominal</td>

   <td width="140">Identifier</td>

  </tr>

  <tr>

   <td width="120">X</td>

   <td width="160">x-coordinate</td>

   <td width="140">Interval</td>

   <td width="140">Feature</td>

  </tr>

  <tr>

   <td width="120">Y</td>

   <td width="160">y-coordinate</td>

   <td width="140">Interval</td>

   <td width="140">Feature</td>

  </tr>

  <tr>

   <td width="120">SpectralCluster</td>

   <td width="160">Cluster Identifier</td>

   <td width="140">Binary</td>

   <td width="140">Target</td>

  </tr>

 </tbody>

</table>




You are asked to use the Support Vector Machine (SVM) algorithm to classify SpectralCluster.  You will use the sklearn.svm.SVC function with the following specifications.

<ol>

 <li>The linear kernel</li>

 <li>The decision function shape is One Over Rest (OVR)</li>

 <li>No limit on the number of iterations</li>

 <li>The random seed is 20200408</li>

</ol>

Please answer the following questions based on your model.

a. What is the equation of the separating hyperplane? Please state the coefficients up to seven decimal places.

b. What is the misclassification rate?

c.  Please plot the y-coordinate against the x-coordinate in a scatterplot. Please color-code the points using the predicted SpectralCluster (0 = Red and 1 = Blue).  Besides, plot the hyperplane as a dotted line to the graph.  To obtain the full credits, you should properly label the axes, the legend, and the chart title.  Also, grid lines should be added to the axes.

d. Please express the data as polar coordinates. Please plot the theta-coordinate against the radius-coordinate in a scatterplot.  Please color-code the points using the SpectralCluster variable (0 = Red and 1 = Blue).  To obtain the full credits, you should properly label the axes, the legend, and the chart title.  Also, grid lines should be added to the axes.

e.You should expect to see three distinct strips of points and a lone point. Since the SpectralCluster variable has two values, you will create another variable, named Group, and use it as the new target variable. The Group variable will have four values. Value 0 for the lone point on the upper left corner of the chart in (d), values 1, 2,and 3 for the next three strips of points.

Please plot the theta-coordinate against the radius-coordinate in a scatterplot.  Please color-code the points using the new Group target variable (0 = Red, 1 = Blue, 2 = Green, 3 = Black).  To obtain the full credits, you should properly label the axes, the legend, and the chart title.  Also, grid lines should be added to the axes.

f.Since the graph in (e) has four clearly separable and neighboring segments, we will apply the Support Vector Machine algorithm in a different way.  Instead of applying SVM once on a multiclass target variable, you will SVM three times, each on a binary target variable.

SVM 0: Group 0 versus Group 1

SVM 1: Group 1 versus Group 2

SVM 2: Group 2 versus Group 3

Please give the equations of the three hyperplanes.

g. Please plot the theta-coordinate against the radius-coordinate in a scatterplot.  Please color-code the points using the new Group target variable (0 = Red, 1 = Blue, 2 = Green, 3 = Black). Please add the hyperplanes to the graph. To obtain the full credits, you should properly label the axes, the legend, and the chart title.  Also, grid lines should be added to the axes

h. Convert the observations along with the hyperplanes from the polar coordinates back to the Cartesian coordinates. Please plot the y-coordinate against the x-coordinate in a scatterplot. Please color-code the points using the SpectralCluster (0 = Red and 1 = Blue). Besides, plot the hyper-curves as dotted lines to the graph.  To obtain the full credits, you should properly label the axes, the legend, and the chart title.  Also, grid lines should be added to the axes.

Based on your graph, which hypercurve do you think is not needed?














