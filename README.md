SOAP CRUD Application



A Spring Boot application implementing a SOAP-based CRUD (Create, Read, Update, Delete) service.



Overview



This project provides a SOAP web service for performing CRUD operations, built using Spring Boot and Spring Web Services. It includes endpoints for managing entities (e.g., users, products) with a backend database (e.g., H2, MySQL).



Prerequisites











Java 17 or higher







Maven 3.6+







Spring Boot 3.x







A database (e.g., H2 for in-memory testing, MySQL for production)







Git







(Optional) IDE like IntelliJ IDEA or VS Code



Setup Instructions











Clone the repository:



git clone https://github.com/Prathamk14/soap-crud-app.git







Navigate to the project directory:



cd soap-crud-app







Configure the database (if using MySQL or another database):











Update src/main/resources/application.properties with your database credentials:



spring.datasource.url=jdbc:mysql://localhost:3306/your\_database

spring.datasource.username=your\_username

spring.datasource.password=your\_password

spring.jpa.hibernate.ddl-auto=update







For H2, no changes are needed if using the default in-memory setup.







Build the project:



mvn clean install







Run the application:



mvn spring-boot:run







Access the SOAP service:











The WSDL is available at: http://localhost:8080/ws/your-service.wsdl







Test endpoints using a SOAP client like Postman or SoapUI.



Features











SOAP endpoints for CRUD operations (e.g., create, read, update, delete entities).







Database integration with JPA/Hibernate (supports H2, MySQL, etc.).







Input validation and error handling.







Configurable via application.properties.



Project Structure



soap-crud-app/

├── src/

│   ├── main/

│   │   ├── java/

│   │   │   └── com/example/soapcrud/ (Java source files)

│   │   └── resources/

│   │       ├── application.properties (Configuration)

│   │       └── wsdl/ (WSDL and XSD files)

├── pom.xml (Maven dependencies)

├── README.md

├── .gitignore



Testing











Use SoapUI or Postman to send SOAP requests to the endpoints.







Example SOAP request for creating a resource:



<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:ex="http://example.com/soapcrud">

&nbsp;  <soapenv:Header/>

&nbsp;  <soapenv:Body>

&nbsp;     <ex:CreateRequest>

&nbsp;        <!-- Add request fields here -->

&nbsp;     </ex:CreateRequest>

&nbsp;  </soapenv:Body>

</soapenv:Envelope>



Contributing











Fork the repository.







Create a feature branch (git checkout -b feature/your-feature).







Commit changes (git commit -m "Add your feature").







Push to the branch (git push origin feature/your-feature).







Open a pull request.



License



MIT License

