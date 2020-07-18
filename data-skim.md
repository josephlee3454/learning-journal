# Step 1: Set up your environment.
* make sure you installed pandas python and jupyter
# Step 2: Import libraries and dataset.
* import 
# Understand the data
* df[df.Code.isin(['GWA_BTC', 'MWA_BTC_JPY', 'MWA_BTC_EUR']) 
   & (df.Date == '2018-01-01')]

# Filter unwanted observations.
* gwa_codes = [code for code in df.Code.unique() if 'GWA_' in code]
* df = df[df.Code.isin(gwa_codes)]

# Pivot the dataset.
* pivoted_df = df.pivot(index='Date', columns='Code', values='VWAP')