# Python
 Python Notes

	Adding autocomplete feature to jupyter notebook
	step 1: Open anaconda prompt and run the following commands
	 1) pip install jupyter_contrib_nbextensions
	 2) pip install jupyter_nbextensions_configurator
	 3) jupyter contrib nbextension install --user 
	 4) jupyter nbextensions_configurator enable --user
 
 
# Python links to learn
 
	https://training.gitbook.io/python-assignments/
	https://training.gitbook.io/web-scraping/
	https://training.gitbook.io/pandas-documents/
	https://training.gitbook.io/pandas-assignments/
	https://www.kaggle.com/datasets/harshitshankhdhar/imdb-dataset-of-top-1000-movies-and-tv-shows
	https://training.gitbook.io/pandas-assignments/imdb-dataset-analysis-basic
	
# Connecting SQL FROM Pandas

	import pandas as pd
	import mysql.connector as mc
	myco = mc.connect(host="database-1.c1qqepuohcck.us-east-2.rds.amazonaws.com",user="admin",passwd="consolefare",database="firstdatabase")
	q = 'select * from saledata'
	df = pd.read_sql(q,myco)
	print(df)