### This is Java Servelet program DAY 1
```java @WebServlet("/hello") ``` -It acts as a Mapping of servelet (it is annotation acts a route).

-@WebServlet: This is a Java annotation used to declare a servlet. Annotations in Java provide metadata about a class, method, or other program elements.  

-("/hello"): This is the URL pattern to which the servlet will respond. In this case, it is "/hello". When a request is made to the URL matching this pattern,
the servlet annotated with @WebServlet("/hello") will be invoked to process the request.  

- It is mandatory to override one of the HTTP method

- There are 3 Methods in servelet
  
  1.**INIT** -
  init(ServletConfig config):
  
  This method is called by the servlet container to initialize the servlet.
  It's typically used for one-time initialization tasks such as loading configuration parameters or establishing database connections.
  The config parameter provides access to the servlet's configuration information.

  2.**DESTROY** -
  destroy():
  
  This method is called by the servlet container when the servlet is being taken out of service, typically during application shutdown or when the container decides to unload the servlet.
  It's used to release any resources held by the servlet, such as closing database connections or releasing file handles.
  This method is invoked only once during the lifecycle of the servlet.
  
  3.**SERVICE** -
  service(ServletRequest request, ServletResponse response):
  
  This method is called by the servlet container to handle client requests.
  It's responsible for processing the incoming request and generating an appropriate response.
  The request parameter represents the client's request, and the response parameter is used to construct and send the response back to the client.
  The default implementation of the service() method in the GenericServlet class dispatches requests to specific HTTP method handlers like doGet(), doPost(), etc., based on the request method (GET, POST, etc.). Subclasses typically override these specific HTTP method handler methods rather than service() itself.
```java
package com.app.pages;

import java.io.IOException;
import java.io.PrintWriter;
import java.time.LocalDateTime;

import javax.servlet.ServletConfig;
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
@WebServlet("/hello")
public class FirstServlet extends HttpServlet {
	@Override
	public void init(ServletConfig config)
	{
		System.out.println("in init "+Thread.currentThread());
	}
	@Override
	public void destroy()
	{
		System.out.println("in destroy "+Thread.currentThread());
	}
	@Override
	public void doGet(HttpServletRequest rq,HttpServletResponse rs) throws ServletException,IOException{
		System.out.println("in do-get "+Thread.currentThread());
		//1. set resp cont type
		rs.setContentType("text/html");
		//2. to send text resp from servlet -> to the clnt  , get writer
		try(PrintWriter pw=rs.getWriter()) {
			//3. generate dyn resp
			pw.print("<h4>Welcome 2 Servlets !"+LocalDateTime.now()+"</h4>");
		}//WC : pw.close -> pw.flush --resp is rendered !
		
	}

}

```
