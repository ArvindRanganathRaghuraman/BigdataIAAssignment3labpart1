# Data Engineering with Notebooks
This repository contains the code for the *Data Engineering with Notebooks* Snowflake Quickstart.

### ➡️ For overview, prerequisites, and to learn more, complete this end-to-end tutorial [Data Engineering with Notebooks](https://quickstarts.snowflake.com/guide/data_engineering_with_notebooks/index.html?index=..%2F..index#0) on quickstarts.snowflake.com.

___
Here is an overview of what we'll build in this tutorial:

<img src="images/quickstart_overview.png" width=800px>

Lab 2 - In Lab 2 we used snowpark and weather data within Snowflake, uploaded the data, and deployed it at the end

![Screenshot 2025-02-20 at 17 47 26](https://github.com/user-attachments/assets/6cf0570a-98ba-4665-8e7b-d1b887652767)
In this screenshot, I have forked the repository as shared by Mr. Jeremiah Hansen to my personal GitHub account. We can see all the files that were shared here

![image](https://github.com/user-attachments/assets/afad4f41-7d4f-4b05-bdb3-8178850adc72)
Within the GitHub workflows folder, we can see the file that is used for deployment, here they have used a yaml file which can be seen here.

![image](https://github.com/user-attachments/assets/27eb6fd3-b374-4dec-9ea2-37ca5756190a)
This is the code within the yaml file which has the instructions on how to deploy the project and has also specified the database and schema from which the deployment will take place.

![image](https://github.com/user-attachments/assets/edc4c103-1dc0-44a8-94ee-8cbfa758e13b)
This is the snowflake screenshot showing the database that we have used and the different schemas under it.
The tables and tasks are created under DEV_SCHEMA where once we 00_start_here notebook all the tables get generated
The tasks get generated once we create a pipeline using Python, a DAG file, and can see the different tables loaded into the pipeline.
In the Integrations schema, we can see the tables with DEMO_EVENTS and a copy of the repository I had forked earlier to my GitHub account.

![image](https://github.com/user-attachments/assets/ac1fd3e2-81d1-41dd-b02a-4345b307dc11)
This is the scripts folder and the files inside it which contains all the SQL commands which we wrote and the code for the deployment file.

![image](https://github.com/user-attachments/assets/e393d657-6839-4315-a12b-ce852685b8a4)
Here we can see the contents within the 06_load_files, which contains the ipynb file and the environment.yaml file within it, when we run this notebook we are taking the excel data and feeding it to the first pipeline to process the data.

![image](https://github.com/user-attachments/assets/b72619e2-0e1f-461b-8263-a4a0f6598ec7)
In this pipeline we do the same process as we did in the first pipeline, but we also take some weather data from the snowflake marketplace which is free to use.


Lab 3

In Lab 3, we explored on how to create native snowflake apps. Native apps help us to publish in marketplace and make it available for wider use.

First, i have cloned the repository given in the labs to my local for the same.

<img width="1356" alt="Screenshot 2025-02-20 at 11 20 50 PM" src="https://github.com/user-attachments/assets/6f342c14-1ae1-4f85-9583-26457068bac6" />

Inside the Repository, the file structure is as follows.

<img width="1443" alt="Screenshot 2025-02-20 at 11 23 38 PM" src="https://github.com/user-attachments/assets/babee145-1cd2-4d1e-8894-fc394c92fc8e" />

The Prepare_data.sh is the script we run to create 3 tables and load data into. The queries for creating and loading the data is in the script file. In order for the consumer to access the data, we have to create it as a reference usage. This is taken care by setup-package-script.sql 

We need to configure the connection to our snowflake instance. For that we need to install snowflake-cli and then run snow connection add. Once done, add the connection details.

Then run the prepare_data.sh script and run the command snow app run. Once the application is created, ensure you give the permission to read the respective tables.

Once done, the app looks like this 

<img width="1366" alt="Screenshot 2025-02-20 at 11 38 31 PM" src="https://github.com/user-attachments/assets/8b2b44d6-8275-4b96-b2bb-d39ab3e78770" />










