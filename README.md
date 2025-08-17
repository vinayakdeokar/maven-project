# Maven CI/CD Project with Jenkins

This repository demonstrates a **Java Maven application** integrated with **Jenkins CI/CD pipeline**.  
The pipeline automates **Build → Test → Package → Deploy** stages using GitHub webhook triggers.

---

## 📌 Project Overview
- **Project 1: maven-build**  
  - Creates a simple Java app (`App.java`, `AppTest.java`)  
  - Build & package with `mvn clean package`  
  - Generates `.jar` file in Jenkins workspace  

- **Project 2: maven-test**  
  - Runs unit tests with `mvn test`  
  - Triggered automatically after Project 1 success  

---

## 🛠️ Tech Stack
- Java 17  
- Maven 3.9+  
- JUnit 5 (Testing)  
- Jenkins (CI/CD)  
- Git & GitHub  

---

## ⚙️ CI/CD Flow
1. Developer pushes code → GitHub repo  
2. GitHub Webhook triggers Jenkins job  
3. **Build Job (maven-build)** → `mvn clean package` → creates JAR  
4. **Test Job (maven-test)** → runs JUnit tests  
5. Successful builds ensure reliable deployments  

---

## 🚀 How to Run Locally
```bash
# Compile & Package
mvn clean package

# Run Tests
mvn test

# Run App
java -cp target/myapp-1.0-SNAPSHOT.jar com.fortune.myapp.App
