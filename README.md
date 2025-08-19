# TASK 8 — Ran a Simple Java Maven Build Job in Jenkins

Built a tiny Java app with **Maven** using a **Jenkins Freestyle** job.

---

## 🎯 Step by Step explanation of what i have done

- Created a Java “Hello World” app with `pom.xml`
- Built it in Jenkins using Maven
- Captured a screenshot of **BUILD SUCCESS**

---

## 🧰 Tools used

- Jenkins (setup locally with a fresh virtual machine)
- Java JDK 17
- Maven 3.9
- Git 

---

## 📂 Project Structure

hello-java-maven/
├── src/
│ └── main/
│ └── java/
│ └── HelloWorld.java
└── pom.xml

---


## 1) Created the project required files in git bash. 

  -- **`src/main/java/HelloWorld.java`**
  -- pom.xml
  
2).  Pushed to GitHub

  -- git init

  -- git add .
  
  -- git commit -m "added new files"
  
  -- git branch -M main
  
  -- git remote add origin https://github.com/Hyghen/hello-java-maven.git

  -- git push -u origin main


3) have set up Jenkins in a fresh Virtual machine

   can access at this url http://192.168.1.9:8080 


4) Configured Maven in Jenkins

Manage Jenkins → Global Tool Configuration

Maven → Add Maven → Name: Maven-3.9.11 → ✔ Install automatically

5) Created the Freestyle Job

New Item → Name: hello-java-maven → Freestyle project → OK

-- Source Code Management

-- Git repo URL (or leave empty if you’ll upload files into workspace)

-- Build → Add build step → Invoke top-level Maven targets

-- Maven Version: Maven-3.9.11

-- Goals: clean package

<img width="1802" height="635" alt="Screenshot 2025-08-19 122456" src="https://github.com/user-attachments/assets/c97b6fcc-50ca-4fe9-9e89-1c414c65ccaa" />


-- Post-build Actions → Archive the artifacts → target/*.jar

-- Save → Build Now


7) Verified the build 

Open Console Output

<img width="1282" height="758" alt="Screenshot 2025-08-19 122352" src="https://github.com/user-attachments/assets/dfc3e584-ef03-4eea-be64-bdae62178ddd" />


<img width="1691" height="533" alt="Screenshot 2025-08-19 122245" src="https://github.com/user-attachments/assets/5071432b-10f4-46f8-92d7-74e06560ee08" />
