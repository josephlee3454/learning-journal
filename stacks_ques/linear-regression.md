# Scikit-learn
* is a powerful python module for machine learning. it contains function for regression, classification, clustering, model selection and dimensionality reduction. 

# import boston data set
#### from sklearn.datasets import load_boston 
#### boston = load_boston()

* The object boston is a dictionary, so you can explore the keys of this dictionary.

# convert boston.data into a pandas data frame.
#### bos = pd.DataFrame(boston.data)
#### bos.head()

# the column names are just numbers, so I am going to replace those numbers with the feature names.
#### bos.columns = boston.feature_names
#### bos.head()

