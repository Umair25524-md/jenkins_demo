# Jenkins Demo Maven Project

This is a minimal Maven Java project intended for demonstrating a Jenkins pipeline.

Structure
- pom.xml
- src/main/java/com/example/App.java
- src/test/java/com/example/AppTest.java
- Jenkinsfile

How to run locally
1. Build and run tests:
   ```bash
   mvn clean test
   ```
2. Run the app:
   ```bash
   mvn -q -DskipTests=true package
   java -cp target/jenkins-demo-1.0.0-SNAPSHOT.jar com.example.App
   ```

Jenkins
- The included Jenkinsfile runs `mvn clean test` and publishes JUnit test results.
