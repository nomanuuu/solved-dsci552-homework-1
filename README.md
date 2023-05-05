Download Link: https://assignmentchef.com/product/solved-dsci552-homework-1
<br>
<h1>1.    Vertebral Column Data Set</h1>

This Biomedical data set was built by Dr. Henrique da Mota during a medical residence period in Lyon, France. Each patient in the data set is represented in the data set by six biomechanical attributes derived from the shape and orientation of the pelvis and lumbar spine (in this order): pelvic incidence, pelvic tilt, lumbar lordosis angle, sacral slope, pelvic radius and grade of spondylolisthesis. The following convention is used for the class labels: DH (Disk Hernia), Spondylolisthesis (SL), Normal (NO) and Abnormal (AB). In this exercise, we only focus on a binary classification task NO=0 and AB=1.<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>

<ul>

 <li>Download the Vertebral Column Data Set from: https://archive.ics.uci.</li>

</ul>

edu/ml/datasets/Vertebral+Column.

<ul>

 <li>Pre-Processing and Exploratory data analysis:

  <ol>

   <li>Make scatterplots of the independent variables in the dataset. Use color to show Classes 0 and 1.</li>

   <li>Make boxplots for each of the independent variables. Use color to show Classes 0 and 1 (see ISLR p. 129). iii. Select the first 70 rows of Class 0 and the first 140 rows of Class 1 as the training set and the rest of the data as the test set.</li>

  </ol></li>

 <li>Classification using KNN on Vertebral Column Data Set

  <ol>

   <li>Write code for k-nearest neighbors with Euclidean metric (or use a software package).</li>

   <li>Test all the data in the test database with <em>k </em>nearest neighbors. Take decisions by majority polling. Plot train and test errors in terms of <em>k </em>for <em>k </em>∈{208<em>,</em>205<em>,…,</em>7<em>,</em>4<em>,</em>1<em>,</em>} (in reverse order). You are welcome to use smaller increments of <em>k</em>. Which <em>k</em><sup>∗ </sup>is the most suitable <em>k </em>among those values? Calculate the confusion matrix, true positive rate, true negative rate, precision, and <em>F</em><sub>1</sub>-score when <em>k </em>= <em>k</em><sup>∗</sup>.<a href="#_ftn2" name="_ftnref2"><sup>[2]</sup></a></li>

  </ol></li>

</ul>

<ul>

 <li>Since the computation time depends on the size of the training set, one may only use a subset of the training set. Plot the <em>best test error rate</em>,<a href="#_ftn3" name="_ftnref3"><sup>[3]</sup></a> which is obtained by some value of <em>k</em>, against the size of training set, when the size of training set is <em>N </em>∈ {10<em>,</em>20<em>,</em>30<em>,…,</em>210}.<a href="#_ftn4" name="_ftnref4"><sup>[4]</sup></a> Note: for each <em>N</em>, select your training set by choosing the first b<em>N/</em>3c rows of Class 0 and the first <em>N </em>−b<em>N/</em>3c rows of Class 1 in the training set you created in 1(b)iii. Also, for each <em>N</em>, select the optimal <em>k </em>from a set starting from <em>k </em>= 1, increasing by 5. For example, if <em>N </em>= 200, the optimal <em>k </em>is selected from {1<em>,</em>6<em>,</em>11<em>,…,</em>196}. This plot is called a <em>Learning Curve</em>.</li>

</ul>

Let us further explore some variants of KNN.

1

<ul>

 <li>Replace the Euclidean metric with the following metrics<a href="#_ftn5" name="_ftnref5"><sup>[5]</sup></a> and test them. Summarize the test errors (i.e., when <em>k </em>= <em>k</em><sup>∗</sup>) in a table. Use all of your training data and select the best <em>k </em>when {1<em>,</em>6<em>,</em>11<em>,…,</em>196}.

  <ol>

   <li>Minkowski Distance:

    <ol>

     <li>which becomes Manhattan Distance with <em>p </em>= 1.</li>

     <li>with log<sub>10</sub>(<em>p</em>) ∈ {0<em>.</em>1<em>,</em>0<em>.</em>2<em>,</em>0<em>.</em>3<em>,…,</em>1}. In this case, use the <em>k</em><sup>∗ </sup>you found for the Manhattan distance in 1(d)iA. What is the best log<sub>10</sub>(<em>p</em>)?</li>

     <li>which becomes Chebyshev Distance with <em>p </em>→∞</li>

    </ol></li>

   <li>Mahalanobis Distance.<a href="#_ftn6" name="_ftnref6"><sup>[6]</sup></a></li>

  </ol></li>

 <li>The majority polling decision can be replaced by weighted decision, in which the weight of each point in voting is <em>inversely proportional </em>to its distance from the query/test data point. In this case, closer neighbors of a query point will have a greater influence than neighbors which are further away. Use weighted voting with Euclidean, Manhattan, and Chebyshev distances and report the best test errors when <em>k </em>∈{1<em>,</em>6<em>,</em>11<em>,</em>16<em>,…,</em>196}.</li>

 <li>What is the lowest training error rate you achieved in this homework?</li>

</ul>

<a href="#_ftnref1" name="_ftn1"></a>