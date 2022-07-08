# Demonetization_analysis
Semantic Analysis of Demonetization project has been developed for the analysis of Indian Demonetization Record. In this project I will find out the views of different people on the demonetization by analysing the tweets from twitter and  will classify the tweets as positive or negative tweets. 

For performing whole process I have used HDFS so firstly I create a directory in HDFS and move the local file to the HDFS and then run the pig script file.

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
