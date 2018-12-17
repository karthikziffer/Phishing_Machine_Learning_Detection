#### Data


The Dataset is a Phishing detection dataset. This dataset consists of input features such as  
**'having_IP_Address', 
'URL_Length',
 'Shortining_Service', 
 'having_At_Symbol', 
 'double_slash_redirecting', 
 'Prefix_Suffix', 
 'having_Sub_Domain', 
 'SSLfinal_State', 
 'Domain_registeration_length',
  'Favicon', 'port', 'HTTPS_token', 
  'Request_URL', 'URL_of_Anchor', 
  'Links_in_tags', 'SFH', 
  'Submitting_to_email', 
  'Abnormal_URL', 
  'Redirect', 
  'on_mouseover', 
  'RightClick', 
  'popUpWidnow', 
  'Iframe', 
  'age_of_domain',
   'DNSRecord', 
   'web_traffic', 
   'Page_Rank', 
   'Google_Index', 
   'Links_pointing_to_page',
   'Statistical_report'** 

The target variable is 
**'Result'**.



---




#### Objective 
The main objective of this project is to develop a predictive model using Machine Learning Algorithms which yields  maximum Test Accuracy on test data.

#### Algorithms Employed:
1. Decision Tree Classifier
2. XG Boost , Cat Boost
3. Random Forest Classifier





#### Procedure

- Since the dataset has categorical data in maximum number of columns, This dataset can fit well with tree based classifier. Since the umique categorical class of columns are limited in number,  tree based classifier would be a good fit for this dataset. 


- The input data is divided into three portions. They are train , val and test.
  Test size was 20% of total dataset. Train size was 80%. Now the train set is further divided to extract val dataset. Hence 25% of train set is divided into val set.

- Here both train and val dataset are of same distribution. If the val dataset accuracy is less than train dataset accuracy. Then the model has high bias.
  If the Test accuracy is less than Train/Val accuracy, then the model has high variance.


##### Decision Tree Classifier
---

- Decision Tree Classifier model predicted a test accuracy of 94%. In this Algorithm, the maximum depth parameter was None(default). Hence the decision tree depth was higher, hence the model stalled to provide higher accuracy. 
- Inadequacy to map the relationship between features since it employs single tree. 

##### Boosting Algorithm ( XG Boost , Cat Boost )
---

- Boosting provides ensemble modeling which takes a sequential method to improve the accuracy of weak model. 
- Boosting algorithm gave a training accuracy of 95%, there was not much difference between boosting algorithm accuracy and random forest without grid search. 







##### Random Forest
---
- Random Forest model incresed the test accuracy above 1% with the number of trees to 10. 
- Because Random Forest multiple tree classification mechanism, which is also called as ensemble. It can classify better by considering all the input features.




##### Random Forest + Grid Search 
- Accuracy of Random Forest Classification can be increased by tunning the hyper-parameters using grid search. Multiple version of experiment was performed to find the optimized hyper-parameter which yeilded an accuray of 96%. 
 - Grid search optimization were performed only on four parameters. They are n_estimators , max_features , max_depth , criterion.
 - N_estimators  represents the number of trees in the forest. Since the number of features are high, higher number of trees can represent greater level of relationships between features.
 - max_features - the maximum number of features considered during split at the tree nodes.  At any particular split, the maximum number of features which makes a decision to split or continue the tree. 
 - max_depth - The maximum depth of the tree. Since longer depth would try to all the feature dependence. Hence higher depth was selected.












