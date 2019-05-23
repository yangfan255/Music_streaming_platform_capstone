# Music_streaming_platform_capstone
Project summary
Musicbox is an anonymous music streaming platform. Customer churn is a key factor limits revenue increase of this platform. Thus, it is critical to identify user who most likely churn, and then recommend songs user might interested to reduce churn rate.

In this project, I have two major goals. First, I built classification models that predict which user will churn (stop using music service) in coming two weeks. Second, various song recommendation engines were constructed based on collaborative filtering.

Data resource
392 files (3.97G size, tar.gz format) from Musicbox were downloaded by using Python Rerequests library.
Each raw file contains daily user information, such as play activity, download history and search history. 
The whole dataset provide 44 days of users activity in the music platform.
All files represents 200K users’ activities for 44 days as well as basic information of 3 million songs. 

Challenges and solutions
1.	A large size of dataset. I pre-processed raw data with shell scripts and sampled 1% data for analysis pipeline building. Spark and SQL were heavily used to visualize and analyze data.
2.	No explicit rating available that users did not rate any songs in the platform. I generated features represent customer behavior such as play activity frequency and latency during different time window. These features were aggregated to re-construct preference of users over songs. 
3.	Evaluation of recommendation system. I built several recommend system such as item similarity and item popularity. SGD and ALS were used to implement recommend purposes
. 
