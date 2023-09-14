# Liquibase-Couchbase demo for CLI deployment
Original changelogs from the extension [repo](https://github.com/liquibase/liquibase-couchbase/tree/dev/test-project)
The repo craeted for the manual source code.


## How to setup the repo locally:
Let's create our first language-independent project with migration step by step. You can use it on different platforms, but Liquibase migrations require JVM on board. Pre-requisites:

We need to install JVM on our machine;

### Step 1.
Install liquibase 4.21.1 version from the [link](https://github.com/liquibase/liquibase/releases/);

Download jar files of provided version and put it into a lib directory in the Liquibase install location (default path: /usr/local/opt/liquibase/lib ).     
- https://mvnrepository.com/artifact/org.liquibase.ext/liquibase-couchbase/0.1.2-ER
- https://mvnrepository.com/artifact/com.couchbase.client/core-io/2.4.6
- https://mvnrepository.com/artifact/com.couchbase.client/java-client/3.4.6
- https://mvnrepository.com/artifact/org.reactivestreams/reactive-streams/1.0.4
- https://mvnrepository.com/artifact/io.projectreactor/reactor-core/3.5.6

### Step 2. 
Configure an administrative user in Couchbase and create a bucket called 'projects.'

### Step 3.
We need to create a working folder; in this example, it is placed in '~/workspace/sandbox/.'

###  Step 4. 
Clone demo repo for the CLI project

``` git clone [https://github.com/rolldeep/liquibase_couchbase_demo](https://github.com/rolldeep/liquibase_couchbase_demo.git) ```

### Step 5.
Go to the liquibase folder and run the command

``` 
cd src/main/resources/liquibase
liquibase update
```

You should see following command output:
```
UPDATE SUMMARY
Run:                          8
Previously run:               0
Filtered out:                 0
-------------------------------
Total change sets:            8

Liquibase: Update has been successful.
Liquibase command 'update' was executed successfully.
```
