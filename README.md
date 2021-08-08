Set Up Details:
------------------

** MySQL DB is being run as a Docker container **
For more details visit: https://phoenixnap.com/kb/mysql-docker-container

Steps to run the application:
    1. After setting up the repo in your local, run the below command from the project root where pom.xml is present
        $  ./mvnw spring-boot:run

API Details:
-----------------

1. POST localhost:8080/demo/add
    The following curl command adds a user (Add unique name)
        $ curl localhost:8080/demo/add -d name=First -d age=18
        Response: Saved
2. GET localhost:8080/demo/all
    The following curl command returns all the users
        $ curl 'localhost:8080/demo/all'
        Response: [{"id":1,"name":"First","age":18}]
3. GET localhost:8080/demo/ageCount
    The following curl command returns age and number of users of that age
        $ curl 'localhost:8080/demo/ageCount'
        Response: {"18":1}
4. GET localhost:8080/demo/nameAndAge
    The following curl command returns name and age of users 
        $ curl 'localhost:8080/demo/nameAndAge'
        Response: {"First":18}

