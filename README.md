README
==========
This is a web page with events searching and preference updating functions.

[Demo page](http://54.149.135.241:8080/ItemRec/) (Please read [Issues](#issues) for more information before demo).

Main Function
---------
1. Supports personalized event recommendation based on favorite records of user.

2. Has flexibility between different API (Ticketmaster and Yelp) and database (MySQL and MongoDB).

Demo Requirements
---------
1. The project can be tested by Apache Tomcat 9 locally and deployed to cloud-computing platform (like Amazon EC2) for online testing.

2. At least one of the database is required (MySQL and MongoDB).

Issues
---------
1. The demo web app may be not that stable to run for many days. Thus, the tomcat will be restarted everyday at 1:00 and 13:00 UTC. The web may be out of service around these time points.

2. The demo web app bases on Yelp API and the app will ask for the geo-location information. If the app cannot get a valid location, it will use a default value.

3. There might be some problems for users who are in the location where Yelp API can not support. These problems can be avoided by rejecting the location-querying request. The app will use default location value instead.

4. (For local test) There are some personal settings that may lead to errors during demo, such as the name or port number of a database. The comments are added above the settings that need to be changed. Like:
```
// update if necessary
```

5. (For local test) The API and database can be changed manually in the file:
```
ItemRec/src/db/DBConnectionFactory.java
```
```
ItemRec/src/external/ExternalAPIFactory.java
```
