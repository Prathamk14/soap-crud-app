📘 SOAP CRUD Application

A Spring Boot SOAP Web Service for managing student records with CRUD (Create, Read, Update, Delete) functionality.

📂 Project Structure
soap-crud-app/
 ├── src/
 │   ├── main/
 │   │   ├── java/com/example/soap/student/   # SOAP Request/Response Classes (JAX-B)  
 │   │   ├── java/com/example/soapcrud/       # Core Application Code  
 │   │   │   ├── config/                      # SOAP Web Service Config  
 │   │   │   ├── controller/                  # SOAP Endpoint Controller  
 │   │   │   ├── entity/                      # Student Entity  
 │   │   │   ├── repository/                  # JPA Repository  
 │   │   │   └── SoapCrudAppApplication.java  # Main Spring Boot App  
 │   │   └── resources/                       # Configurations & XML schemas  
 ├── pom.xml                                  # Maven Dependencies  
 └── README.md                                # Documentation

🚀 Features

✅ SOAP Web Service built with Spring Boot

✅ Student Entity with CRUD operations

✅ Endpoints for:

Add Student

Get Student by ID

Get All Students

Update Student

Delete Student

✅ Integrated with JPA Repository for persistence

🛠️ Tech Stack

Backend: Spring Boot, Spring Web Services

Data Binding: JAXB (for SOAP XML)

Database: JPA / Hibernate (configurable to H2, MySQL, PostgreSQL)

Build Tool: Maven

Language: Java

⚙️ Installation & Setup

Clone the repository

git clone https://github.com/Prathamk14/soap-crud-app
cd soap-crud-app


Build the project using Maven

mvn clean install


Run the application

mvn spring-boot:run


Access WSDL (Web Service Definition)

http://localhost:8080/ws/students.wsdl

📌 Example SOAP Requests
➕ Add Student
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:stu="http://example.com/soap/student">
   <soapenv:Header/>
   <soapenv:Body>
      <stu:AddStudentRequest>
         <stu:name>John Doe</stu:name>
         <stu:age>22</stu:age>
         <stu:email>john@example.com</stu:email>
      </stu:AddStudentRequest>
   </soapenv:Body>
</soapenv:Envelope>

📖 Get Student by ID
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:stu="http://example.com/soap/student">
   <soapenv:Header/>
   <soapenv:Body>
      <stu:GetStudentRequest>
         <stu:id>1</stu:id>
      </stu:GetStudentRequest>
   </soapenv:Body>
</soapenv:Envelope>

✅ Testing

Run unit tests with:

mvn test
