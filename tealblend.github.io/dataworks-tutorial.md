Dataworks Tutorial
---------

Dataworks is an IBM service that allows developers, data analyst, and business analyst to easily manage data preparations with ease through the use of their cloud based user interface. It allows to refine their data that fits their needs easily so that it saves them more time in refining data and more time in analyzing it.

In this tutorial we would need the following:

 - Dataworks Service
 - Any database service (e.g. dashDB, )

> Note: For this tutorial, we would be using dashDB service since it already contains sample data that we can use to manipulate with Dataworks.

#### **Adding Dataworks and dashDB service** ####

 1. On your dashboard, click the **`Services and APIs`**.

 2. Look for **`IBM Dataworks`** and **`dashDB`** and add them to your dashboard.
 

> Note: You do not have to bind your Dataworks and dashDB to any application.

####**Exploring IBM Dataworks**####
1. Click the IBM Dataworks service that is found in your dashboard.

2. Click the **`Manage`** button. 

3.  You will then see a menu on the left side of the screen which are Tasks, Browse, Admin , and Help.

4. Tasks section contains Refine and Copy, Publish, Create Connection. We will be only focusing on **`Refine and Copy`** and **`Create Connection`**.

5. The Browse section contains three functions namely Activities, Datasets, and Connections. Only **`Activities`** and **`Connections`** will be used in this tutorial.

6. The Admin part allows a database service to send its contents to different database service (e.g. dashDB to DB2). However, this service requires installation of another software so it will not be part of the tutorial.

#### **Establishing a connection to dashDB in Dataworks** ####

> Note: It is advisable to open two windows for this part. One for dashDB service and the second one is for the Dataworks.

 1. Click the **`Create Connection`** that is under **`Tasks`**.
 
 2. From there you would see different database service that Dataworks can connect to, click on the IBM dashDB .
 
 3. Upon clicking, it would ask for some information such as username password and the host name.
 
 4. Go to the window where your dashDB is located and click the **`Service Credentials`**.
 
 5. You would the information of your dashDB credentials in JSON format but only a few of them is needed by Dataworks to connect specifically the "db"(database name), 'username', "host", "password". You can copy those information and paste them in the necessary field if the values are too long to type.
 
 6.  Add a name to your connection and description(optional).
 
 7. Once finished click the **`Create Connection`** button.

####**Refining Your Data in IBM Dataworks**####
