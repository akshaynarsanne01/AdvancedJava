## What is web container
  Web container is serverside Java Virtual Machine , It provides run time Environment to web applications.
  ### Jobs : 
  - Manages lifecycle of web Apps.
  - Creates server request and response objects.
  - Manages session Tracking
  - Manages Concurrency

## What & Why servelets 
Java Servlets are the Java programs that run on the Java-enabled web server or application server. They are used to handle the request obtained from the web server, process the request, produce the response, and then send a response back to the web server. 
It adds dynamic nature to the web applications.
  ### Jobs :
  - Request Processing
  - Dynamic response generation
  - Business Logic
  - Managing Data Access Layer (DAO)
  - Page navigation

![image](https://github.com/akshaynarsanne01/Advaned-Java/assets/147087536/d8584bda-11ea-4c64-a9c2-25feabf6b8e3)

## Deployment Of servelet
There are two methods
### ANNOTATIONS :
 ```java
 @WebServlet(value = "/login", loadOnStartup = 1)
public class LoginServlet extends HttpServlet {
}
```
This ```@WebServlet``` is a class level annotation. when we are deploying the application java compiler adds this into the Hashmap
later it gets executed as per the need by in the run time.
Map : will be created by web container
Key : URL pattern ```/hello```
Value : Fully Qualified Servlet class name ```com.app.myservlet.LoginServlet```
