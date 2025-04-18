## Run a Simple Java Maven Build Job in Jenkins -----Task 8

## Objective:
- The goal of this task is to learn how to use Jenkins to build a simple Java application using Maven. This will be your first step into Continuous Integration/Continuous Delivery (CI/CD).

## Tools Required:

- Jenkins (installed locally or via Docker)
- Java JDK 8 or 11
- Apache Maven
- Git (optional — can run from local folder)

##  Deliverables:
- A basic Java HelloWorld app (with pom.xml).
- Jenkins Freestyle job configured to build it.
- Screenshot of successful build console output.

## Sample Dataset/Repo:
- Repository name: hello-java-maven
- Contents:
          - src/main/java/HelloWorld.java
          - pom.xml

### HelloWorld.java

This is a simple Java class that outputs a message to the console:

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Jenkins + Maven!-------Task 8");
    }
}
```

## pom.xml

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.example</groupId>
    <artifactId>hello</artifactId>
    <version>1.0</version>

    <build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>3.8.1</version>
                <configuration>
                    <source>1.8</source>
                    <target>1.8</target>
                </configuration>
            </plugin>
        </plugins>
    </build>
</project>
```
## 3 To run Jenkins using Docker

- docker run -p 8080:8080 jenkins/jenkins:lts
## 4. Set Up Jenkins
## Install Required Tools
- Maven: Go to Manage Jenkins → Global Tool Configuration. Under the Maven section, click Add Maven and configure it:

- Name: Maven (e.g., Maven 3.9.9)

- Install Automatically: Check this option to install Maven automatically if it's not already installed.

- Java: Similarly, ensure that JDK is configured in the Global Tool Configuration page (Add JDK, e.g., JDK 11).

## Create a New Freestyle Project
- Go to Jenkins Dashboard → New Item.

- Enter the name of the project (e.g., Java Maven Build Task-8) and select Freestyle project.

- Click OK.

## Configure the Freestyle Project
In the Build section:
           - Select Invoke top-level Maven targets.

Set Goals to clean package.

Optionally, if you are using Git, you can add the Git repository URL under Source Code Management.

## 5. Build the Project
- After configuring the job, click Save.

- On the job page, click Build Now.

Jenkins will start building your project using Maven. You can monitor the progress by clicking on the Build Number under the Build History section.

## Screenshots
## 1.Creating a Folder
![1](https://github.com/user-attachments/assets/89968570-9d5f-4098-8e2d-428b9046d6d3)

--------------------------
## 2.Creating a .java and .xml file
![2](https://github.com/user-attachments/assets/d157a243-91ed-4cef-a2d8-cd9fff498806)

--------------------------
## 3.Running a jenkins using Docker image
![3](https://github.com/user-attachments/assets/7c35e60d-1c94-41ca-aced-9ea13e42da61)

--------------------------
## 4.Project push to Github
![4](https://github.com/user-attachments/assets/20586026-31e4-441b-bc4e-e73ae4537ad6)

--------------------------
## 5.Output of the java code
![5](https://github.com/user-attachments/assets/ddc4e30c-4c85-4974-ae99-08cbe10c2bb0)

--------------------------
## 6.Build Completed in jenkins
![7](https://github.com/user-attachments/assets/7aaa7f9a-a5c5-4f68-af56-6ff46c95713a)

--------------------------
## 7.BUILD SUCCESS
![6](https://github.com/user-attachments/assets/7dcf3a22-fbaf-4553-a69e-ce348fe81429)












