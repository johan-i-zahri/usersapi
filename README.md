# userapi
Java Spring Boot Demo  

# Scope of work
A program that will: 
1. Do search and export maximum of 100 Users from Github into PDF Format. 
2. Do list of export history and able to download existing pdf
Program specification as below:
1. Use REST API endpoint to perform export PDF (any endpoint name is fine)
2. Use REST API endpoint to perform list of export history
3. Use REST API endpoint to download existing exported PDF
4. Defined Json Request Payload and  Postman collection
5. Defined Json Response of bad response/no record found
6. Use JAVA with Spring Boot Framework
7. Good Code Structure
8. Good Naming Convention
9. Create JUnit Test to handle code coverage
10. Create MySQL database if required to stored exported PDF history
Reference Github Public API to integrate (Or can find similar API):  
https://docs.github.com/en/rest/search?apiVersion=2022-11-28#search-users

# Setup your eclipse ide to enable lombok
Please follow the instructions in this url:  
https://projectlombok.org/setup/eclipse

# To open project using Eclipse
1. Import project from git with the url -> https://github.com/johan-i-zahri/usersapi.git  
	you will need to Import it as a general project by doing the following:  
	File > Import  
	> choose/type Projects from Git  , next  
	> choose Clone URI  , next  
	> https://github.com/johan-i-zahri/usersapi.git and credentials , next  
	> choose all branch, next  
	> choose target directory, choose main as inital branch, next  
	> choose import as general, next  
	> finish  
2. Convert the imported project into maven project by right clicking the project and choose  
	Configure > Convert to Maven Project
3. The debugging configuration should be automatically loaded. To access them goto:  
	Debug icon drop down > Debug Configurations...  
	
# To setup the database
Run the extras/sql/db.sql to create the database schema  
Run the extras/sql/tables.sql to create the tables  

the default settings  
user: root  
password: admin

to change credential settings, edit the file:  
src/main/resources/application.properties  
* spring.datasource.username=root
* spring.datasource.password=admin

# To run the coverage test 
Right click on the project and go to Coverage As>JUnit Test  

If you would like to run the coverage against live test use the following:  
Right click on the project and go to Coverage As>Java Application  

Do not terminate the instance so as to retain the coverage data,  
instead use the shutdown postman collection action or follow the link:  
http://localhost:8000/shutdown-app

The default port to run is 8000, configured in the application.properties
* server.port=8000

# To import the postman collection
Use the files in extra/postman/test.postman_collection.json

# To clean and compile the application
Debug icon drop down > Debug Configurations...  
choose Maven Build > usersapi-clean-compile


# To run the applications
Debug icon drop down > Debug Configurations...  
choose Java Application > Application



# STATUS UPDATE

Till 20230313 I have able to implement all the functionalities required.  
Test cases for coverage have only been implemented for basic functionalities of  
all the controllers (ExportController, ExportHistoryController)  
and only some services (ExportService)

If time allows I will update the rest.
