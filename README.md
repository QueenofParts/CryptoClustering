# CryptoClustering
Module 11 Challenge

Motivation:
My motivation in this working on this challenge is to practice and solidify several concepts including dataframes, scaling, the Kmeans and Principal Compnent Analysis (PCA) functions, and the use of timeframes.  I worked on this with other students in the class to help all of us share our questions, observations and ideas with one another as we learn collaboratively. - "You find yourself with someone else."

The focus of this exercise:
This project provides an opportunity to examine price changes of cryptocurrencies over intervals spanning 24 hours, 7 days, 30 days, 60 days, 200 days, and 1 year. This classification and analysis will be conducted using the K-means algorithm and principal component analysis (PCA)


Table of Contents:   

Table of Contents:
Installation
Usage
Credits
License

Installation
Installation instructions to be added.

Usage
This code is to be run on Mac or PC with the following tools installed:  

Pandas
Scikit Learn:  KMeans
Scikit Learn: PCA
Scikit Learn: StandardScaler
matplotlib
seaborn
hvplot
numpy


![alt text](assets/images/screenshot.png)
Credits and Types of help:
My collaborators for this project are:

• Farzana Azad-Hussain (add link to github profile)

With many thanks to them for time spent, Farzana provided the following help:

• understanding the nuances of the assignment 

• helping one another recognize proper use use the new concepts we are leaning 

• spotting and correcting errors
Websites and other Sorces:
###Websites:

During the work on this this assignment, my colaborators and I used the following websites for reminders of the syntax and structure of certain commands and clarificatrion regarding the specifics of their use:

• Chat GPT -- www.chatgpt.com

• GeeksforGeeks -- www.geeksforgeeks.com

• SciKit Learn -- https://scikit-learn.org/

• CoPilot


Books:
I also referred to the following books for reminders, symtax rules and guidence regarding Python commands:

• “The Python Workshop, 2nd ed” (Packt, 2022) Bird, Han, Jiminez, Lee and Wade

• "Python Crash Course, 2nd Edition" (no starch press, 2019) Mathes
Applications and Extensions:
• GitBash

• VSCode

• Copilot

• Black Formatter

Video Tutorials:


License:
The last section of a high-quality README file is the license. This lets other developers know what they can and cannot do with your project. If you need help choosing a license, refer to https://choosealicense.com/.

🏆 The previous sections are the bare minimum, and your project will ultimately determine the content of this document. You might also want to consider adding the following sections. Badges

Badges aren't necessary, per se, but they demonstrate street cred. Badges let other developers know that you know what you're doing. Check out the badges hosted by shields.io. You may not understand what they all represent now, but you will in time. Features If your project has a lot of features, list them here. How to Contribute If you created an application or package and would like other developers to contribute it, you can include guidelines for how to do so. The Contributor Covenant is an industry standard, but you can always write your own if you'd prefer. Tests Go the extra mile and write tests for your application. Then provide examples on how to run them here.

# Module 11 Challenge Instructions and Rubric:

Due: Jan 25 at 11:59pm

Calendar	Bootcamp: OSU-VIRT-AI-PT-10-2023-U-LOLC-MWT

Details

In this Challenge, you’ll apply your understanding of the K-means algorithm and principal component analysis (PCA) to classify cryptocurrencies according to their price fluctuations across various timeframes. Specifically, you will examine price changes over intervals spanning 24 hours, 7 days, 30 days, 60 days, 200 days, and 1 year.

Before You Begin
Create a new repository for this project called CryptoClustering. Do not add this homework to an existing repository.

Clone the new repository to your computer.

Push your changes to GitHub.

Files
Download the following files to help you get started:

Module 11 Challenge files

Instructions
Rename the Crypto_Clustering_starter_code.ipynb file as Crypto_Clustering.ipynb.

Load the crypto_market_data.csv into a DataFrame and set the index to the “coin_id” column.

Get the summary statistics to see what the data looks like before proceeding.

Prepare the Data
Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

The first five rows of the scaled DataFrame should appear as follows:

The first five rows of the scaled DataFrame.
Find the Best Value for k Using the Original Scaled DataFrame
Use the elbow method to find the best value for k by completing the following steps:

Create a list with the number of k values from 1 to 11.
Create an empty list to store the inertia values.
Create a for loop to compute the inertia with each possible value of k.
Create a dictionary with the data to plot the elbow curve.
Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
Answer the following question in your notebook: What is the best value for k?
Cluster Cryptocurrencies with K-Means Using the Original Scaled Data
Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:

Initialize the K-means model with the best value for k.
Create an instance of K-means, define the number of clusters based on the best value of k, and then fit the model using the original scaled DataFrame.
Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
Create a copy of the original data and add a new column with the predicted clusters.
Create a scatterplot using pandas’ plot as follows:
Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
Optimize Clusters with Principal Component Analysis
Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.

Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:

What is the total explained variance of the three principal components?
Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

The first five rows of the PCA DataFrame should appear as follows:

The first five rows of the PCA DataFrame.
Find the Best Value for k Using the PCA Data
Use the elbow method on the PCA data to find the best value for k using the following steps:

Create a list with the number of k-values from 1 to 11.
Create an empty list to store the inertia values.
Create a for loop to compute the inertia with each possible value of k.
Create a dictionary with the data to plot the elbow curve.
Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
Answer the following questions in your notebook:
What is the best value for k when using the PCA data?
Does it differ from the best k-value found using the original data?
Cluster Cryptocurrencies with K-Means Using the PCA Data
Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:

Initialize the K-means model with the best value for k.
Create an instance of K-means, define the number of clusters based on the best value of k, and then fit the model using the PCA data.
Predict the clusters to group the cryptocurrencies using the PCA data.
Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
Create a scatte rplot using pandas’ plot as follows:
Set the x-axis as "PC1" and the y-axis as "PC2".
Answer the following question:
What is the impact of using fewer features to cluster the data using K-Means?
Determine the Weights of Each Feature on Each Principal Component
Create a DataFrame that shows the weights of each feature (column) for each principal component by using the columns from the original scaled DataFrame as the index.

Which features have the strongest positive or negative influence on each component?

Requirements
Find the Best Value for k Using the Original Scaled DataFrame (15 points)
To receive all points, you must:

Code the elbow method algorithm to find the best value for k. Use a range from 1 to 11. (5 points)

Visually identify the optimal value for k by plotting a line chart of all the inertia values computed with the different values of k. (5 points)

Answer the following question: What’s the best value for k? (5 points)

Cluster Cryptocurrencies with K-Means Using the Original Scaled Data (10 points)
To receive all points, you must:

Initialize the K-means model with four clusters by using the best value for k. (1 point)

Fit the K-means model by using the original data. (1 point)

Predict the clusters for grouping the cryptocurrencies by using the original data. Review the resulting array of cluster values. (3 points)

Create a copy of the original data, and then add a new column of the predicted clusters. (1 point)

Using pandas’ plot, create a scatter plot by setting x="price_change_percentage_24h" and y="price_change_percentage_7d". (4 points)

Optimize the Clusters with Principal Component Analysis (10 points)
To receive all points, you must:

Create a PCA model instance, and set n_components=3. (1 point)

Use the PCA model to reduce the features to three principal components, then review the first five rows of the DataFrame. (2 points)

Get the explained variance to determine how much information can be attributed to each principal component. (2 points)

Answer the following question: What’s the total explained variance of the three principal components? (3 points)

Create a new DataFrame with the PCA data. Be sure to set the coin_id index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame. (2 points)

Find the Best Value for k by Using the PCA Data (10 points)
To receive all points, you must:

Code the elbow method algorithm, and use the PCA data to find the best value for k. Use a range from 1 to 11. (2 points)

Visually identify the optimal value for k by plotting a line chart of all the inertia values computed with the different values of k. (5 points)

Answer the following questions: What’s the best value for k when using the PCA data? Does it differ from the best value for k that you found by using the original data? (3 points)

Cluster the Cryptocurrencies with K-Means by Using the PCA Data (10 points)
To receive all points, you must:

Initialize the K-means model with four clusters by using the best value for k. (1 point)

Fit the K-means model by using the PCA data. (1 point)

Predict the clusters for grouping the cryptocurrencies by using the PCA data. Review the resulting array of cluster values. (3 points)

Create a copy of the DataFrame with the PCA data, and then add a new column to store the predicted clusters. (1 point)

Using pandas’ plot, create a scatter plot by setting x="PC1" and y="PC2". (4 points)

Determine the Weights of Each Feature on Each Principal Component (15 points)
To receive all points, you must:

Create a DataFrame that shows the weights of each feature (column) for each principal component by using the columns from the original scaled DataFrame as the index. (10 points)

Answer the following question: Which features have the strongest positive or negative influence on each component? (5 points)

Coding Conventions and Formatting (10 points)
To receive all points, you must:

Place imports at the top of the file, just after any module comments and docstrings, and before module globals and constants. (3 points)

Name functions and variables with lowercase characters, with words separated by underscores. (2 points)

Follow DRY (Don't Repeat Yourself) principles, creating maintainable and reusable code. (3 points)

Use concise logic and creative engineering where possible. (2 points)

Deployment and Submission (10 points)
To receive all points, you must:

Submit a link to a GitHub repository that’s cloned to your local machine and that contains your files. (4 points)

Use the command line to add your files to the repository. (3 points)

Include appropriate commit messages in your files. (3 points)

Code Comments (10 points)
To receive all points, your code must:

Be well commented with concise, relevant notes that other developers can understand. (10 points)
Grading
This project will be evaluated against the requirements and assigned a grade according to the following table:

Grade	Points
A (+/-)	90+
B (+/-)	80–89
C (+/-)	70–79
D (+/-)	60–69
F (+/-)	< 60
Submission
To submit your Challenge assignment, click Submit, and then provide the URL of your GitHub repository for grading.

note
You are allowed to miss up to two Challenge assignments and still earn your certificate. If you complete all Challenge assignments, your lowest two grades will be dropped. If you wish to skip this assignment, click Next, and move on to the next module.

Comments are disabled for graded submissions in Bootcamp Spot. If you have questions about your feedback, please notify your instructional staff or your Student Success Manager. If you would like to resubmit your work for an additional review, you can use the Resubmit Assignment button to upload new links. You may resubmit up to three times for a total of four submissions.

important
It is your responsibility to include a note in the README section of your repo specifying code source and its location within your repo. This applies if you have worked with a peer on an assignment, used code in which you did not author or create sourced from a forum such as Stack Overflow, or you received code outside curriculum content from support staff such as an Instructor, TA, Tutor, or Learning Assistant. This will provide visibility to grading staff of your circumstance in order to avoid flagging your work as plagiarized.

If you are struggling with a challenge assignment or any aspect of the academic curriculum, please remember that there are student support services available for you:

Ask the class Slack channel/peer support.

AskBCS Learning Assistants exists in your class Slack application.

Office hours facilitated by your instructional staff before and after each class session.

Tutoring Guidelines - schedule a tutor session in the Tutor Sessions section of Bootcampspot - Canvas

If the above resources are not applicable and you have a need, please reach out to a member of your instructional team, your Student Success Advisor, or submit a support ticket in the Student Support section of your BCS application.
