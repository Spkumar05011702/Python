# Python
 Python Notes

	Adding autocomplete feature to jupyter notebook
	step 1: Open anaconda prompt and run the following commands
	 1) pip install jupyter_contrib_nbextensions
	 2) pip install jupyter_nbextensions_configurator
	 3) jupyter contrib nbextension install --user 
	 4) jupyter nbextensions_configurator enable --user
	 
	 
# Pandas funtion Unique Values in all categorical columns 
	def unique_val(df):
	  cat=df.select_dtypes(include="object").nunique().sort_values(ascending = False).index
	  ndf=pd.DataFrame()
	  for i in cat:
	    ndf[f'{i}']=pd.Series(df[f'{i}'].unique())
	  ndf.replace(np.nan,"",inplace=True)
	  return ndf.T

 
# Python links to learn
 
	https://training.gitbook.io/python-assignments/
	https://training.gitbook.io/web-scraping/
	https://training.gitbook.io/pandas-documents/
	https://training.gitbook.io/pandas-assignments/
	https://www.kaggle.com/datasets/harshitshankhdhar/imdb-dataset-of-top-1000-movies-and-tv-shows
	https://training.gitbook.io/pandas-assignments/imdb-dataset-analysis-basic
	https://docs.consoleflare.com/

  	https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/5834576229597553/3860602172662271/8862019661831722/latest.html
	df = df.withColumn('DateDiff', expr("(Date2 - Date1)")) df = df.withColumn('DateDiff', df['DateDiff'].cast("integer")) 

(Funtion-UDF)-
https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/1061712452516424/1911494012811915/8153847934095880/latest.html

Bad Data handling
 databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/1061712452516424/3636884342836401/8153847934095880/latest.html
 
# Connecting SQL FROM Pandas

	import pandas as pd
	import mysql.connector as mc
	myco = mc.connect(host="database-1.c1qqepuohcck.us-east-2.rds.amazonaws.com",user="admin",passwd="consolefare",database="firstdatabase")
	q = 'select * from saledata'
	df = pd.read_sql(q,myco)
	print(df)
