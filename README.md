# python-github-api
Demonstrating the extraction of information from GitHub Account.  

# Problem Statment
Find top 5 most popular repositories of any account(I am using "google" here) on github (https://github.com/google) based on the number of forks. For each such repo find the top 3 committees and their commit counts. 

# We can solve this problem with two approaches
1: Logic One:
This logic does not need any authentication for accessing data. Reading all github pages from any repositories/account using pandas

Syntax: json_response =pandas.read_json(url)

Drawback: GitHub API "https://api.github.com/" can allow to hit only 60 Request in one hour for particular IP Address

2: Logic Two:
To solve the above problem we use "Requests" instead of "read_json" a Pandas inbuilt function, which needs authentication for accessing the GitHub API. Once we get the HTML data then convert it into Pandas Dataframe.

Syntax: requests.get(url,auth=(USER_ID,PASS)).content

##Note
We are going to solve this problme with second approach, where you need to provide your github credentials.
