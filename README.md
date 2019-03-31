Project Title
A Movie Recommendation Engine with Spark ML on Amazon EMR

Getting Started
Need to download JaiswalRodeShahShah.zip file which consist of 
- Executable MOVIE.Jar file
- personalRating.txt file

Prerequisites
- We have run this code on AWS EMR configured of Spark 2.3 using 2.11 version.
- Download the Dataset from https://drive.google.com/drive/u/1/folders/1wmnQbJwVqPM7d4KJd9Fw5rPZXZZBqmJ4?ogsrc=32.

Installing

1) Create S3 bucket on AWS.
2) Copy all the dataset and Jar file on S3 bucket.
3) Congigured AWS EMR with Spark Version 2.10.
4) Follow the instruction of SSH after creating a cluster on AWS to connect AWS EMR from local machine.
5) Copy all the files from S3 to EMR cluster using aws s3 cp s3://<bucketname>/<files> <local path of cluster>
6) Copy all the Dataset files to Hadoop DFS of EMR using hdfs dfs -put <local path of data files> <HDFS file location>
7) For ALS : 
	"spark-submit --class MovieLensALS MOVIES.jar <HDFS path dir> personalRatings.txt"
8) For CosineSimilarities :
	"spark-submit --class ItemSimiarities_new MOVIES.jar <movieID for which we need recommendation>"


Build 
We use SBT to build the jar files consist of 2 classes.

Authors
Darshan Shah
Shashikant Jaiswal
Parays Rode
Ashay Shah

Report Link
https://webpages.uncc.edu/prode1/

