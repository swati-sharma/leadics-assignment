Set Up Details:
------------------

**MySQL DB is being run as a Docker container**

For more details visit: https://phoenixnap.com/kb/mysql-docker-container

Steps to run the application:

    1. After setting up the repo in your local, run the below command from the project root where pom.xml is present

        $  ./mvnw spring-boot:run

API Details:
-----------------

1. POST localhost:8080/demo/users

    The following curl command adds a user (Add unique name)

        $ curl localhost:8080/demo/users -d name=First -d age=18

        Response: Saved

2. GET localhost:8080/demo/users

    The following curl command returns all the users

        $ curl 'localhost:8080/demo/users'

        Response: [{"id":1,"name":"First","age":18}]

3. GET localhost:8080/demo/users/ages

    The following curl command returns the age and the number of users of that age

        $ curl 'localhost:8080/demo/users/ages'

        Response: {"18":1}

4. GET localhost:8080/demo/users/namesWithAge

    The following curl command returns the name and the age of users 

        $ curl 'localhost:8080/demo/users/namesWithAge'

        Response: {"First":18}

