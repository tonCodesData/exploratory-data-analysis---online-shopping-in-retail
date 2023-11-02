# Exploratory Data Analysis of Online Shopping in Retail
Assuming the role of Data Analyst for a large retail company, I take on the task to conduct exploratory data analysis on a dataset of online shopping website activity. With the increasing popularity of online shopping, this dataset provides valuable insights into consumer behaviour.

I use various statistical and visualisation techniques to explore the data and draw meaningful insights. My analysis not only provide a better understanding of customer behaviour but also help the business optimise marketing strategies and improve their customer experience.

The data contains information about the website activity of users over one year. Each sample represents the user interacting with the website during a shopping session.

Overall, this project showcases my prowess in exploratory data analysis in uncovering valuable insights from large datasets and how I can leverage these insights to drive business success.

Technologies and Dependencies: Python, AWS

### Milestone 1: Extract the online shopping data from the cloud
I create Python classes to extract online shopping data from a database in the cloud and get familirised with the data before moving on to performing data cleaning tasks and Exploratory Data Analysis. 
#### Task 1: Initialise a class to extract the data
##### Step 1: 
Create a new Python script db_utils.py which will contain the code to extract the data from the database.
##### Step 2: 
Within the script create a new class called RDSDatabaseConnector. 
This class will contain the methods which will be used to extract data from the RDS database.
#### Extract data from the RDS database
The online shopping data is stored in an AWS RDS database. You will need to create the methods which will enable you to extract the data from this database.
##### Step 1: 
Create a credentials.yaml file to store the database credentials.

Remember to add this file to your .gitignore file in your repository, as you don't want your credentials being pushed to GitHub for security reasons.

Add the following credentials to your credentials.yaml file which will allow you to connect to the remote database:

RDS_HOST: eda-projects.cq2e8zno855e.eu-west-1.rds.amazonaws.com
RDS_PASSWORD: EDAonlinecustomer
RDS_USER: onlinecustomeranalyst
RDS_DATABASE: web_data
RDS_PORT: 5432


##### Step 2: 
If you haven't already installed Python PyYAML package you should do so before the next step. This can be installed by running pip install PyYAML in the terminal and imported using import yaml. This will allow you to load your credentials.yaml file as a dictionary.


##### Step 3: 
After installing the package create a function which loads the credentials.yaml file and returns the data dictionary contained within. This will be be passed to your RDSDatabaseConnector as an argument which the class will use to connect to the remote database.


##### Step 4: 
Write the __init__ method of your RDSDatabaseConnector class. It should take in as a parameter a dictionary of credentials which your function from the previous step will extract.


##### Step 5: 
Define a method in your RDSDatabaseConnector class which initialises a SQLAlchemy engine from the credentials provided to your class. This engine object together with the Pandas library will allow you to extract data from the database.


##### Step 6: 
Develop a method which extracts data from the RDS database and returns it as a Pandas DataFrame. The data is stored in a table called customer_activity.


##### Step 7: 
Now create another function which saves the data to an appropriate file format to your local machine. This should speed up loading up the data when you're performing your EDA/analysis tasks. The function should save the data in .csv format, since we're dealing with tabular data.

### Milestone 2: Exporatory Data Analysis
In this step, I perform Exploratory Data Analysis (EDA) on the online shopping data. I gain a deeper understadning of the data and identify any patterns which might exist. I also identify any issues such as missing or incorrectly formatted data. Then I apply statistical techniques to gain insight on the data's distribution and apply visualisation techniques to identofy patters or trends in the data.   

### Milestone 3: Analysis and Visualisation
Now the data has been transformed, I provide deeper insights from the data. I dive deeper into the dataset to identify any patterns or trends not visible by previous analysis. By gaining deeper insights, management can make more informed decisions about changes to the website and marketing strategies. 
