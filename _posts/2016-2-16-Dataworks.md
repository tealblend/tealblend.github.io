---
layout: post
---


Dataworks is an IBM service that allows developers, data analyst, and business analyst to easily manage data preparations with ease through the use of their cloud based user interface. It allows to refine their data that fits their needs easily so that it saves them more time in refining data and more time in analyzing it.
 
In this tutorial we will need the following:
 
   Dataworks Service
   Any database service (e.g. dashDB, Cloudant, DB2)
 
 > For this tutorial, we will be using dashDB service since it already contains sample data that we can use to manipulate with Dataworks.
 
##Adding Dataworks and dashDB service##
 
  1. On your dashboard, click the `Services and APIs`.
 
  2. Look for `IBM Dataworks` and `dashDB` and add them to your dashboard.

  
 
> You do not have to bind your Dataworks and dashDB to any application.

> Additional step for dashDB service: You need to go to the dashboard of dashDB by clicking the service then click `Launch` and go `TABLES` tab. Create your default schema using `ADD TABLE` and just click `RUN DDL` in order to create the default user schema automatically.

##**Exploring IBM Dataworks**##
 1. Click the IBM Dataworks service that is found in your dashboard.
 
 2. Click the `Manage` button then click the left arrow button. 
 
 3.  You will then see a menu on the left side of the screen which are Tasks, Browse, Admin , and Help.
 
 4. Tasks section contains Refine and Copy, Publish, Create Connection. We will be only focusing on `Refine and Copy` and `Create Connection`.
 
 5. The Browse section contains three functions namely Activities, Datasets, and Connections. Only `Activities` and `Connections` will be used in this tutorial.
 
 6. The Admin part allows a database service to send its contents to different database service (e.g. dashDB to DB2). However, this service requires installation of another software so it will not be part of the tutorial.
 
##**Establishing a connection to dashDB in Dataworks**##
 
  > It is advisable to open two windows for this part. One for dashDB service and the second one is for the Dataworks.

 
  1. Click the `Create Connection` under `Tasks` section.
  
  2. From there you will see different database service that Dataworks can connect to, click on the IBM dashDB .
  
  3. Upon clicking, it will ask you information such as username password and the host name.
  
  4. Go to the window where your dashDB is located and click the `Service Credentials`.
  
  5. You will see the information of your dashDB credentials in JSON format but only a few of them is needed by Dataworks to connect specifically the "db"(database name), 'username', "host", "password". You can copy those information and paste them in the necessary field if the values are too long to type.
  
  6.  Add a name to your connection and description(optional).
  
  7. Once finished click the `Create Connection` button.
 
##**Selecting the data for refinement**##
 1 . Click the `Refine and Copy` under the Task section.
 
 2 . Choose the dashDB connection that you have just created and you will see several schemas inside dashDB.
 
 3 . We will be using the sample schema created by dashDB which is `GOSALESHR`. 
 
 4 . Click `GOSALESHR` and check the `EMPLOYEE` table by clicking on the box. 
 
 5 .  Click the `REFINE` button.
 
##**Exploring the data refinement page**##
 
 Once you are on the next page you should see your EMPLOYEE table loaded with its contents and on top of it is the information regarding the table. The first column tells how many the table has in total, the second one is the data type present in the table, the third one tells you the overall quality of the table if it is ready to be used for analysis or not, and the last shows the number of rows or data inside the table.
 
 On the left side of the table sheet you will see four options named columns, metrics, history, and join. Columns allow you to hide and unhide certain columns, metrics allow you to see the individual quality of the columns, the history is where you will see all the changes you have made and join lets you combine twoo or more tables into one.
 
##**Refining Your Data in IBM Dataworks**##
1. Click the `Metrics` option and check the quality of each column.

2. Go to the `Termination Date` column and you will notice it has a low quality and Dataworks will tell you that it has a lot of missing values or null values. (You can also click the column and click `Properties` to show the details of that column)

3. Click the `Termination Date` name and click `Filter`. (You will see different values under that column and we will filter out the missing values)

4. Click  `Invert` and uncheck the `[NULL]` value and click the `Filter` button.

5. You will notice that the overall data quality got higher and the number of rows was obviously reduced. 

6.  Go to the `FIRST_NAME` column and click it. 

7.  Click `Sort` and tick `ascending` and click `SORT`.

8. You will see that there is a duplicate in the first name which is **Alexandra** .

9. Remove the duplicate by clicking `FIRST_NAME` again and click `Remove Duplicates`. (Do not click anything in the options and proceed by clicking `Remove Duplicates` button)  

10. Go to the `GENDER_CODE` column and you will see that it only has a value of 0 or 1 for either male of female.

11. Remove the column by clicking `Remove Column`.

##**Joining Two Tables**##

1. Click the `Add` button on the top left side of the page.

2. Go to `GOSALESHR` schema and `EMPLOYEE_HISTORY` table and click `Add`.

3. You can do whatever you want in the new table you have added and proceed to the next step once you are satisfied.

4.  Go back to `EMPLOYEE` table and click `Join` on the left. (You can deselect or select any columns you like and just click join once your are done)

5.  You will the part wherein it will ask you to select a column that you will use to match the two tables together which is very similar to what you are doing back in SQL.

6. Click the box beside A and B and choose `EMPLOYEE_CODE` as your matching column.

7. Below there are four options to combine which are Matching Rows, A+Matching Rows, B+Matching Rows, and All Rows. They are the counterpart of the join command that you used in SQL (INNER JOIN,, LEFT JOIN, RIGHT JOIN, FULL JOIN). 

8.   Choose Matching Rows and click Join.

> After joining the two tables you will now see that the information above the table sheet changed such as the overall quality and the total columns.

##**Save and Run Your Activity**##

> It is required to give a name to your activity before your proceed which can be seen on top of the page.

1. Click the `NEXT` button.

2. Select the target connection which you have created choose the user schema (DASH******) and click the radiobutton for "I want replace data".

3.  Click `Run` .

> You can also click Save first and run your created activity later.

 4. Once you click `Run` wait for a few seconds and it will tell if the process is successful or not
 
 5. You can view your refined data from the schema DASH******.


-End of Tutorial- 

