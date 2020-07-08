# object creation 
* creating a series by passing a list of values, letting pandas create a default integer index:
* IN:
#### s = pd.Series([1,3,5, np.nan, 6, 8])
#### s
* OUT:
#### 0 1.0
#### 1 3.0
#### 2 5.0
#### 3 NaN
#### 4 6.0
#### 5 8.0
#### dtype: float64
# create a data frame by passing a NumPy array w. a dateline index and labeled columns 
* IN:
#### dates = pd.date_range ('20130101', periods=6)
#### dates 
* OUT:
#### DatetimeIndex(['2013-01-01', '20130102', '2013-01-03', '2013-01-4', '2013-01-05', '20-13-01-06'])
* IN: df = pd.DataFrame(np.random.randn(6, 4), index=dates, columns=list('ABCD'))

* IN: df
#### A     B        C       D
#### 2013-01-01  0.469112 -0.282863 -1.509059 -1.135632
#### 2013-01-02  1.212112 -0.173215  0.119209 -1.044236
#### 2013-01-03 -0.861849 -2.104569 -0.494929  1.071804
#### 2013-01-04  0.721555 -0.706771 -1.039575  0.271860
#### 2013-01-05 -0.424972  0.567020  0.276232 -1.087401
#### 2013-01-06 -0.673690  0.113648 -1.478427  0.524988
# Selection by label
* getting a cross section using a label
* IN: 
#### df.loc[dates[0]]
* OUT: 
#### A    0.469112
#### B   -0.282863
#### C   -1.509059
#### D   -1.135632
#### Name: 2013-01-01 00:00:00, dtype: float64

* selecting on a multi-axis by label:
* In : df.loc[:, ['A', 'B']]
* Out: 
#### A            B
#### 2013-01-01  0.469112 -0.282863
#### 2013-01-02  1.212112 -0.173215
#### 2013-01-03 -0.861849 -2.104569
#### 2013-01-04  0.721555 -0.706771
#### 2013-01-05 -0.424972  0.567020
#### 2013-01-06 -0.673690  0.113648