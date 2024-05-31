# Java EE (Enterprise Edition) 8 (J2EE 1.8) & Jakarta EE 8

Welcome to the Java EE (Enterprise Edition) 8 (J2EE 1.8) and Jakarta EE 8 repository! This document provides an overview of Java EE 8 and its core concepts.

## What is J2EE?

J2EE, or Java Enterprise Edition, consists of specifications defining essential services required for enterprise applications. These include Servlet API, JSP (Java Server Page) API, Security, Connection pooling, EJB (Enterprise Java Bean), JNDI (Java Naming and Directory Interface), JPA (Java Persistence API), JMS (Java Messaging Service), Java Mail, Java Server Faces, Java Transaction API, Webservices support (SOAP/REST), and more.

### Key Points:
- **Enterprise Application (EA):** A large software platform designed for corporate environments, typically server-side, transactional, and multi-threaded.
- **Vendor of J2EE Specs:** Oracle/Sun/Eclipse.
- **Implementation:** Left to vendors (J2EE server vendors).
- **J2EE Compliant Servers:** Apache Tomcat (web server), Glassfish (reference implementation), JBoss (wildfly), Oracle WebLogic, IBM WebSphere, and more.

## Why J2EE?

1. **Support for Various Clients:** Thin clients (web), thick clients (Java applications), and smart clients (mobile).
2. **Server Independence:** Applications developed in J2EE can run on any J2EE compliant server, ensuring consistent behavior.
3. **Ready-made Implementations:** Primary services like security, connection pooling, etc., are readily available, allowing developers to focus on business logic.

## HTTP Request-Response Flow Layers:

1. Web browser
2. Web server
3. Web Container (server-side JVM)
4. Web Application (HTML/JSP/Servlet)

## Dynamic Web Applications:

These are server-side applications deployed on a web server, typically meant for servicing web clients using HTTP/HTTPS protocols.

## Web Container (WC) and Its Jobs:

The Web Container is a server-side JVM residing within a web server. It's responsible for managing the lifecycle of dynamic web components, handling HTTP requests and responses, providing support for services like naming, security, and connection pooling, and managing concurrent requests.

## What is web.xml?

It serves as the deployment descriptor for a web application, containing deployment instructions read by the Web Container at deployment time. It includes deployment instructions like welcome page, servlet deployment tags, session configuration, security configuration, etc.

## Servlets:

Servlets are Java classes representing dynamic web components whose lifecycle is managed by the Web Container. They handle request processing, business logic, dynamic response generation, data access logic, and page navigation.

### Objective 1: Test Basic Servlet Lifecycle
- Creating and deploying a Hello Servlet.
- Deployment options: Via annotation or legacy approach using XML tags.

### Objective 2: Test Basic Servlet Lifecycle (deployed via XML)
- Reading request parameters sent from the client.

### Objective 3: Accept Different Types of Inputs from User
- Writing a servlet to display request parameters or starting with a case study.

### Objective 4: Servlet JDBC Integration

---

Feel free to explore the code and documentation in this repository to understand and utilize Java EE 8 and Jakarta EE 8 effectively in your enterprise applications.
