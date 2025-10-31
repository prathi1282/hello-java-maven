# ☕ Hello Java Maven with Jenkins  
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)]()  
[![Jenkins](https://img.shields.io/badge/Jenkins-CI%2FCD-blue)]()  
[![Maven](https://img.shields.io/badge/Maven-Build-orange)]()  

A simple Java **Hello World** project built using **Maven** and automated with **Jenkins Freestyle Job**.

---

## 📁 Project Structure

hello-java-maven/
├── src/
│ └── main/
│ └── java/
│ └── HelloWorld.java
└── pom.xml


---

## 🧠 Overview
This project demonstrates:
- How to use **Jenkins** to build a Java project with **Maven**.  
- Basic **CI/CD** concepts with Jenkins Freestyle jobs.  
- A simple Java program that prints `"Hello, Jenkins + Maven!"`.

---

## ⚙️ Setup Instructions

### 1️⃣ Create Java App
**src/main/java/HelloWorld.java**
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Jenkins + Maven!");
    }
}

2️⃣ Start Jenkins

Run Jenkins in Docker:

docker run -d --name jenkins -p 8080:8080 jenkins/jenkins:lts


Open Jenkins at http://localhost:8080
 and complete setup.

3️⃣ Configure Maven in Jenkins

Go to Manage Jenkins → Global Tool Configuration

Add Maven (e.g., Maven 3.8.6)

4️⃣ Create a Freestyle Job

New Item → Freestyle Project → Name it hello-java-maven

Under Build, select Invoke top-level Maven targets

Set Goal: clean package

Save and click Build Now

5️⃣ Verify the Build

Open Console Output → You should see:

[INFO] BUILD SUCCESS

✅ Output

A successful Maven build for the Java HelloWorld app using Jenkins.


