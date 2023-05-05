Download Link: https://assignmentchef.com/product/solved-cse6363-project-3-logistic-regression
<br>
<h1></h1>

<ol>

 <li>Consider the polynomial fit problem where you want to find the best polynomial approximation of order <em>k </em>to a set of data points.</li>

 <li>Implement the polynomial fit solver for 2-dimensional input data as a linear regression learner.Remember, that in order for linear regression to build a non-linear regression function – such as a higher order polynomial – you need to design the correct non-linear features and represent the data in terms of those features before applying the linear regression algorithm. Make sure your implementation can handle polynomial fits of different order (at least to 4th order).</li>

 <li>Apply your regression learner to the following data set (you can download the dataset as a file fromCanvas) , list the learned parameters, and plot the resulting function for order 1, 2, 3, and 4. Plot the resulting polynomial surface together with the data points (using your favorite plotting program, e.g. Matlab, Octave, gnuplot, …)</li>

</ol>

<em>D </em>= { ((6<em>.</em>4432<em>,</em>9<em>.</em>6309)                  50<em>.</em>9155)<em>,            </em>((3<em>.</em>7861<em>,</em>5<em>.</em>4681)            29<em>.</em>9852)<em>,</em>

((8<em>.</em>1158<em>,</em>5<em>.</em>2114)            42<em>.</em>9626)<em>,            </em>((5<em>.</em>3283<em>,</em>2<em>.</em>3159)            24<em>.</em>7445)<em>,</em>

((3<em>.</em>5073<em>,</em>4<em>.</em>8890)            27<em>.</em>3704)<em>,            </em>((9<em>.</em>3900<em>,</em>6<em>.</em>2406)            51<em>.</em>1350)<em>,</em>

((8<em>.</em>7594<em>,</em>6<em>.</em>7914)            50<em>.</em>5774)<em>,            </em>((5<em>.</em>5016<em>,</em>3<em>.</em>9552)            30<em>.</em>5206)<em>,</em>

((6<em>.</em>2248<em>,</em>3<em>.</em>6744)                31<em>.</em>7380)<em>,         </em>((5<em>.</em>8704<em>,</em>9<em>.</em>8798)                     49<em>.</em>6374)<em>, </em>((2<em>.</em>0774<em>,</em>0<em>.</em>3774)    10<em>.</em>0634)<em>,                   </em>((3<em>.</em>0125<em>,</em>8<em>.</em>8517)                     38<em>.</em>0517)<em>, </em>((4<em>.</em>7092<em>,</em>9<em>.</em>1329)    43<em>.</em>5320)<em>,         </em>((2<em>.</em>3049<em>,</em>7<em>.</em>9618)                   33<em>.</em>2198)<em>, </em>((8<em>.</em>4431<em>,</em>0<em>.</em>9871)    31<em>.</em>1220)<em>,         </em>((1<em>.</em>9476<em>,</em>2<em>.</em>6187)                     16<em>.</em>2934)<em>, </em>((2<em>.</em>2592<em>,</em>3<em>.</em>3536)                   19<em>.</em>3899)<em>,         </em>((1<em>.</em>7071<em>,</em>6<em>.</em>7973)                     28<em>.</em>4807)<em>, </em>((2<em>.</em>2766<em>,</em>1<em>.</em>3655)    13<em>.</em>6945)<em>,         </em>((4<em>.</em>3570<em>,</em>7<em>.</em>2123)                   36<em>.</em>9220)<em>, </em>((3<em>.</em>1110<em>,</em>1<em>.</em>0676)    14<em>.</em>9160)<em>,         </em>((9<em>.</em>2338<em>,</em>6<em>.</em>5376)                     51<em>.</em>2371)<em>, </em>((4<em>.</em>3021<em>,</em>4<em>.</em>9417)                   29<em>.</em>8112)<em>,         </em>((1<em>.</em>8482<em>,</em>7<em>.</em>7905)                     32<em>.</em>0336)<em>, </em>((9<em>.</em>0488<em>,</em>7<em>.</em>1504)    52<em>.</em>5188)<em>,         </em>((9<em>.</em>7975<em>,</em>9<em>.</em>0372)                   61<em>.</em>6658)<em>, </em>((4<em>.</em>3887<em>,</em>8<em>.</em>9092)    42<em>.</em>2733)<em>,         </em>((1<em>.</em>1112<em>,</em>3<em>.</em>3416)                     16<em>.</em>5052)<em>, </em>((2<em>.</em>5806<em>,</em>6<em>.</em>9875)                   31<em>.</em>3369)<em>,         </em>((4<em>.</em>0872<em>,</em>1<em>.</em>9781)                     19<em>.</em>9475)<em>, </em>((5<em>.</em>9490<em>,</em>0<em>.</em>3054)    20<em>.</em>4239)<em>,         </em>((2<em>.</em>6221<em>,</em>7<em>.</em>4407)                   32<em>.</em>6062)<em>, </em>((6<em>.</em>0284<em>,</em>5<em>.</em>0002)    35<em>.</em>1676)<em>,         </em>((7<em>.</em>1122<em>,</em>4<em>.</em>7992)                     38<em>.</em>2211)<em>, </em>((2<em>.</em>2175<em>,</em>9<em>.</em>0472)                   36<em>.</em>4109)<em>,         </em>((1<em>.</em>1742<em>,</em>6<em>.</em>0987)                     25<em>.</em>0108)<em>,</em>

((2<em>.</em>9668<em>,</em>6<em>.</em>1767)                       29<em>.</em>8861)<em>,         </em>((3<em>.</em>1878<em>,</em>8<em>.</em>5944)                     37<em>.</em>9213)<em>, </em>((4<em>.</em>2417<em>,</em>8<em>.</em>0549)    38<em>.</em>8327)<em>,  </em>((5<em>.</em>0786<em>,</em>5<em>.</em>7672)                     34<em>.</em>4707)          }

<ol>

 <li>c) Evaluate your polynomial regression functions by computing (and showing) the error on the following data points (generated from the original function). You can download the data points as a file from Canvas. Compare the error results and try to determine for what polynomials overfitting might be a problem<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>. Which order polynomial would you consider the best prediction function and why ?</li>

</ol>

<h2>CSE 6363 – <em>Machine Learning </em>Project 1: Regression</h2>

<h1>Logistic Regression</h1>

<ol start="2">

 <li>Consider again the problem from the first assignment where we want to predict the gender of a person from a set of input parameters, namely height, weight, and age. Assume the same training data:</li>

</ol>

<h2><em>D </em>= { ((170<em>,</em>57<em>,</em>32)<em>,           W</em>)<em>, </em>((190<em>,</em>95<em>,</em>28)<em>,                M</em>)<em>, </em>((150<em>,</em>45<em>,</em>35)<em>,     W</em>)<em>, </em>((168<em>,</em>65<em>,</em>29)<em>,                M</em>)<em>, </em>((175<em>,</em>78<em>,</em>26)<em>,     M</em>)<em>, </em>((185<em>,</em>90<em>,</em>32)<em>,                 M</em>)<em>, </em>((171<em>,</em>65<em>,</em>28)<em>,     W</em>)<em>, </em>((155<em>,</em>48<em>,</em>31)<em>,                W</em>)<em>,</em></h2>

((165<em>,</em>60<em>,</em>27)<em>, W</em>)<em>, </em>((182<em>,</em>80<em>,</em>30)<em>, M</em>)<em>, </em>((175<em>,</em>69<em>,</em>28)<em>, W</em>)<em>, </em>((178<em>,</em>80<em>,</em>27)<em>, M</em>)<em>, </em>((160<em>,</em>50<em>,</em>31)<em>, W</em>)<em>, </em>((170<em>,</em>72<em>,</em>30)<em>, M</em>)<em>, </em>}

<ol>

 <li>Implement logistic regression to classify this data (the individual data elements, i.e. height, weight,and age, as features. Your implementation should take different data sets as input for learning.</li>

 <li>Use your logistic regression function to predict the classes for the same data items as in the firsthomework:</li>

</ol>

(162<em>,</em>53<em>,</em>28)<em>,</em>(168<em>,</em>75<em>,</em>32)<em>,</em>(175<em>,</em>70<em>,</em>30)<em>,</em>(180<em>,</em>85<em>,</em>29)

Given that the correct class labels for these items are <em>W,M,W,M</em>, respectively, compare the results for your logistic regression with the ones for KNN (from your first assignment). Discuss what differences exist and why Logistic Regression can yield better results for this problem.

<a href="#_ftnref1" name="_ftn1">[1]</a> Remember that overfitting occurs when the algorithm starts modeling not only the function but also the noise. This usually results in lower error on the training set but higher error on the test data (data it has not been trained with).

Manfred Huber                                                                                                                                                                              Page 1