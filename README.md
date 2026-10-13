# Event Hub: Campus Events Management System

A Java Servlet and JSP web application where students browse and join campus events and an administrator publishes and manages them. Built with Java, Maven and MySQL between March 2024 and June 2024.

> This is a **showcase repository**. The source code lives in a private repository. This page documents what the project does and how it is built. Happy to walk through the code on request.
>
> Student portfolio project. There is no live demo and no automated test suite.

[LinkedIn](https://linkedin.com/in/ratnesh-pathak-087466279) | [Email](mailto:pathakratnesh03@gmail.com)

## Preview

![Event Hub home page](screenshots/event-hub-ui.jpg)

## What Is Implemented

| Area | Status |
| --- | --- |
| Registration and login with salted PBKDF2 password hashes | Implemented |
| Browse new and old events, filter by category (Cultural, Arts and Creative, Innovations, Competitions) | Implemented |
| Event details and participation in active events | Implemented |
| View and delete your own participations | Implemented |
| Submit, list and delete your own feedback | Implemented |
| Edit your profile (requires your password) | Implemented |
| Help-line page | Implemented |
| Admin area: add events with image upload, edit name and status, delete events | Implemented |
| Admin views of all participants and all feedback | Implemented |
| Event search | A search page exists, but it is not linked from the navigation |

## Tech Stack

- **Backend:** Java 8, Servlets 4.0, JSP, JSTL, plain JDBC with a DAO layer
- **Build:** Maven (WAR), runs on Apache Tomcat 9
- **Database:** MySQL
- **Frontend:** HTML5, CSS3, JavaScript, Bootstrap 4

## Security Measures in the Source

- No database credentials in code, with settings read from environment variables or a properties file
- Server-side authorization for admin pages and for actions that change data
- CSRF tokens on POST requests, with deletes done as POST forms
- Output escaping in the JSP pages and prepared statements for SQL
- Image uploads checked by extension and file signature, with a size limit

These measures reduce risk. They do not make the application completely secure.

## Limitations

- No live demo, and it is not hosted
- No automated tests
- Bootstrap 4.0.0 and jQuery 3.2.1 are old versions
- No login rate limiting, password reset or email verification
- No database connection pool
- Uploaded images are stored inside the deployed web app

## Author

Ratnesh Pathak - M.Sc. Information Technology, AI / ML Engineer, Founder of Team Ignites

GitHub: [@RatneshPathak](https://github.com/RatneshPathak) | LinkedIn: [Ratnesh Pathak](https://linkedin.com/in/ratnesh-pathak-087466279) | Email: pathakratnesh03@gmail.com

(c) Ratnesh Pathak. All rights reserved. The text and images in this repository may not be reused without permission.
