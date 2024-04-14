# Students performance and difficulties prediction

   This academic project is about using machine learning algorithms to predict whether or not a student would pass the final exam. 
   The data set used is from UCI Machine Learning Repository.

 
# Introduction

  Education is an important element of the society, every government and country in the world work so hard to improve this sector. With the corona-virus outbreak that has disrupted life around the globe in 2020, the educational systems have been affected in many ways; studies show that student’s performance has decreased since then, which highlights the need to deal with this problem more seriously and try to find effective solutions, as well as the influencing factors.  


 and solve the problems.


# Dataset processing

Now before training themodel the need is to process the data :

1) Need to map each string to a numerical value so that it can be used for model training.
       
       Example to make this clear : The mother job column contain five values : 'teacher', 
       'health','services', 'at_home' and 'other'.
      
       Job then is to map each of these string to numerical values, and this is how it's done :
       df['Mjob'] = df['Mjob'].map({'teacher': 0, 'health': 1, 'services': 2, 'at_home': 3, 'other': 4})
        
    </br>    
        
        
2) Need to perform feature scaling :

        	Feature scaling is a method used to normalize the range of independent variables 
		or features of data. In data processing, it is also known as data normalization 
		and is generally performed during the data preprocessing step.
        
		This will allow learning algorithms to converge very quickly. The operation requires 
		to take each column, let's say 'col', and replace it by :
        
    ![\Large](https://latex.codecogs.com/svg.latex?\Large&space;col=\frac{col-mean(col)}{max(col)})
    
    		But this is not the only scaling you can do, you can try also :
		
    ![\Large](https://latex.codecogs.com/svg.latex?\Large&space;col=\frac{col-mean(col)}{std(col)}), where **std**  refers to standard deviation.
    
:warning: **We will not perform feature scaling for binary columns that contains 0's and 1's** .


# Dataset visualization  

   After having the processed dataset, the next step is dataset visualization; so that patterns, trends and correlations that might not otherwise be detected can be now exposed.

   This discipline will give some insights into the data and help to understand the dataset by placing it in a visual context using python libraries such as: matplotlib and seaborn.

   There are so many ways to visualize a dataset. In this project the used ones are: 
   
      #1- Plot distribution histograms so that we can see the number of samples that occur in 
      each specific category.
      E.g.  Internet accessibility at home distribution shows that our dataset consists of 
      more than 300 students with home internet accessibility, 
      while there are about 50 students who have no access to the internet at home.
      
      #2- Plot “Boxplots” to see to see how the students status is distributed according to each variable.
      
      #3- Plot the correlation output that should list all the features and their correlations 
      to the target variable.
      So that we have an idea about the most impactful elements on the students status. 



# Model evaluation (metrics)


Before starting training our classifers define the metrics that will be used to compare between our three classifiers :

    1) Confusion matrix :
    
<img src='https://miro.medium.com/max/2102/1*fxiTNIgOyvAombPJx5KGeA.png' width='440cm'>

    2) F1 score :
    
<img src = 'https://www.gstatic.com/education/formulas2/-1/en/f1_score.svg' width='440cm'>

TP = number of true positives <br>
FP = number of false positives <br>
FN = number of false negatives <br>

    3) The roc curve :
     A receiver operating characteristic curve, or ROC curve, 
    is a graphical plot that illustrates the diagnostic ability of a binary 
    classifier system as its discrimination threshold is varied. 


<img src ='https://upload.wikimedia.org/wikipedia/commons/thumb/3/36/Roc-draft-xkcd-style.svg/800px-Roc-draft-xkcd-style.svg.png' width='500cm'>


    4) ROC score : it's simply the value of the area under the roc curve. 
    The best value is 1 because the area of 1x1 square is 1.


<br>
Starting by the first learning algorithm :
<br>


# Logistic regression


# KNN
 



# SVM

<h4>2) Comparison :</h4>


Now, after training our three svm models, it is better to group all the results so it can be easy to compare between them :


<br>

Now after we train our three models, here are the metrics and the ROC plots :


This table contains all metrics :


|<span style="color:red">Metric | <span style="color:red">Linear kernel |<span style="color:red">polynomial kernel  |<span style="color:red">gaussian kernel|
| ----------------|---------------|-------------------|:-------------:|
| training time   |   11ms   	  |     7ms	      |      3ms      |
| accuracy %      | 84.375       |   78.125          |    82.8125     |
| confusion matrix|[15 8]<br>[2 39| [12 8]<br>[6 38] |[10 11]<br>[0 43]|
| f1 score        |  0.82         |        0.74       |    0.77       |
| roc_auc_score   |  0.80         |      0.73         |      0.74     |




<h4>3) The more accurate svm classifier :</h4>


As you can see the training times are soo small thanks to feature scaling. As you can also notice, the best svm model the one that used the linear kernel. So let's show the results of this linear kernel svm model again :

**The training time** : <b><span style="color:red">11ms </span><br></b>
**The accuracy** : <b><span style="color:red">84.375 % </span><br></b>
**The f1 score** : <b><span style="color:red">0.82 </span><br></b>
**The roc_auc_score** : <b><span style="color:red">0.8</span><br></b>

	As you can see the accuracy is pretty good for our problem, but we need to see also 
	that the f1 score has a high value so the model performed very well on the test set. 
	Our model is able to generlize for new data and get good prediction. 
	The value of the area under the roc curve is approximatly 0.80 which is good, 
	this tells us that the model is capable of distinguishing between the two classes.


<h4>4) Factor extaction :</h4>

After validating our model, lets extract the positive and negative factors, in the iPython notebook we explained very well how we managed to do that :

After calling the appropriate function, we got:

---------------------------------------------------------------------
Factors helping students succeed :<br>
    
    parents education 
    guardian
    wants to take higher education
    studytime
    parents job
---------------------------------------------------------------------
Factors leading students to failure :<br>
    
    age
    health
    going out with friends
    absences
    failures
    

# Conclusion

   