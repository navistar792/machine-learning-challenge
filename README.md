# machine-learning-challenge

### Preprocess the data
* ML Data Cleanup.ipynb was used to format the data and to utput a csv file that could be used for all the other analyses
* Used `dtypes` to identify any non-integer fields
* Used `drop` to remove object columns not important to the analysis
* Used `dropna` to remove columns that only have blank values, and to remove rows with blanks* exported a clean csv with headers and no index
#### In subsequent steps, a separate Jupyter Notebook file was used for each model, Including: 
* Use of `MinMaxScaler` to scale the numerical data.
* Separating the data into training and testing data using `train_test_split`


### Tune Model Parameters

* Used `GridSearch` to tune model parameters.
* Tune and compare at least two different classifiers. For the SVM model I used `C` and `gamma` and for Random Forest Models I used `max_depth` and `n_estimators`

### SVM and Random Forest Classifier models were used
* SVM was the least accurate model, with a test accuracy after hypertuning of 0.88. 

* For the Random Forest Classifier models, Recursive Feature Elimination was used to find the optimum number of features

* for Random Forest Classifier (RFC)  models, the original number of features (41) as well as 25 features reached 90% test accuracy. 

* Unlike the SVM model, Hyperparameter tuning made no improvements to the accuracy of the RFC models with 41 and 25 features.

* I'm assuming the RFC model with 25 features would be the best choice, since it has the same accuracy as using all features, and may result in better model performance?

#### Table 1

<table>
<tr>
<th>Model</th>
<th>Initial Test Accuracy</th>
<th>After HPT</th>
</tr>
<tr>
<td>SVM</td>
<td>0.83</td>
<td>0.88</td>
</tr>
<tr>
<td>RFC (41 features)</td>
<td>0.90</td>
<td>0.90</td>
</tr>
<tr>
<td>RFC (30 Features)</td>
<td>0.89</td>
<td>0.89</td>
</tr>
<tr>
<td><b>RFC (25 Features)</b></td>
<td><b>0.90</td>
<td><b>0.90</td>
</tr>
<tr>
<td>RFC (20 Features)</td>
<td>0.89</td>
<td>0.89</td>
</tr>
<tr>
<td>RFC (15 Features)</td>
<td>0.89</td>
<td>0.89</td>
</tr>
<tr>
<td>RFC (5 Features)</td>
<td>0.87</td>
<td>0.87</td>
</tr>
</table>

* With an accuracy of 90%, the RFC 25 model should be good enough to correctly predict new exoplanets!

    