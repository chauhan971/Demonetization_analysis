# Demonetization_analysis
Semantic Analysis of Demonetization project has been developed for the analysis of Indian Demonetization Record. In this project we will find out the views of different people on the demonetization by analysing the tweets from twitter and we will classify the tweets as positive or negative tweets. You can find the demonetization twitter data in data folder.

For performing whole process I will use HDFS so firstly you have to create a directory in HDFS and move the local file to the HDFS and then run the pig script file.
You can find twitter as well as reting dictionary data into the data folder

Command to run project :

# Createing directory in HDFS to store csv and rating dictionary file

$ hadoop fs -mkdir /demion_analysis

# Moveing  local file to the HDFS. 

$ hadoop fs -copyFromLocal /home/dark/data/demonetization-tweets.csv /demion_analysis
$ hadoop fs -copyFromLocal /home/dark/data/AFINN.csv /demion_analysis

# Executeing the pig script 

$ pig -x mapreduce /home/dark/demonotetization_analysis.pig

# Checking positive and negative tweets 

$ hadoop fs -cat /demion_anaysis/positive_tweets/*00 

$ hadoop fs -cat /demion_anaysis/negative_tweets/*00 
