# Startup Tutorial for GoGato

### Prerequisites:
* Java 8
* An internet browser
* Visual Studio Code
* Docker or IntelliJ (with Amazon Corretto 8 JDK)

---

### **Backend Setup:**

#### _Docker Method_ -
> 1. Download and Install Docker

> 2. Pull User service image: **marcusg73/gogatouser**

> 3. Pull Post service image: **marcusg73/gogatopost**

> 4. Create/run a container for the User service based on the User service image with the command: **docker run -dt -p 8000:8000 marcusg73/gogatouser**

> 5. Create/run a container for the Post service based on the Post service image with the command: **docker run -dt -p 8081:8081 marcusg73/gogatouser**

> 6. See "Frontend Setup" for continued instruction

> ***Possible Issue(s)***:
> - Images may not exist if pulling docker image doesn't work
> - Images were created with a live database meaning the database may not be active/exist at the time of container creation, in which case, use the IntelliJ method

#### _IntelliJ Method_ -

> 1. Download and install IntelliJ

> 2. Clone User service repository: https://github.com/Revature-GoGato/GoGatoUsers.git

> 3. Clone Post service repository: https://github.com/Revature-GoGato/GoGatoPostsBackend.git

> 4. Open both services in IntelliJ as separate windows/projects

> 5. Run both services in IntelliJ as separate applications

> 6. See "Frontend Setup" for continued instruction

> ***Possible Issue(s)***:

> For User service -
> - The application.properties may be set to "prod" profile
To solve this, remove the "spring.profiles.active" line as well as database info, approx. lines 17-22 

> For Post service -
> - The application.properties may contain database info
To solve this, remove the database info approx. lines 1-6

---

### **Frontend Setup:**
> If this link doesn't work while the backend is running, follow steps 1-5 below: https://gogatotest.vercel.app/

> 1. Download and install VS Code

> 2. Clone frontend repository: https://github.com/Revature-GoGato/GoGatoFrontEnd.git

> 3. Run npm install command via command line inside directory where repo was cloned

> 4. Run npm start command via command line inside directory where repo was cloned

> 5. Browser will open when application is ready


---