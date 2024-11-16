Contact Management System
Project Overview
The Contact Management System is a Java-based application designed to manage and organize contact information effectively. It allows users to perform CRUD (Create, Read, Update, Delete) operations on contact data, stored in a MongoDB database, ensuring a flexible and scalable backend.

Features
Add Contacts: Save new contacts with details like Name, Phone, and Email.
View Contacts: Retrieve and display a list of all saved contacts.
Update Contacts: Modify details of existing contacts.
Delete Contacts: Remove outdated or unnecessary contacts.
Search Contacts: Search for specific contacts based on provided details.
Technologies Used
Programming Language: Java
Editor: Visual Studio Code
Database: MongoDB
Libraries/Frameworks:
MongoDB Java Driver
JSON Parsing Library (if required)
Version Control: Git
Prerequisites
Ensure the following tools are installed:

Java Development Kit (JDK) (version 8 or higher)
VS Code with the Java Extension Pack
MongoDB Community Server (running locally or accessible remotely)
Git
Setup and Installation
Clone the repository to your local machine:

bash
Copy code
git clone https://github.com/ashwaniprajapati049/Contact-management.git  
Open the project in VS Code:

Navigate to the folder using File > Open Folder.
Install the MongoDB Java Driver:

Add the dependency to your pom.xml (if using Maven):
xml
Copy code
<dependency>  
    <groupId>org.mongodb</groupId>  
    <artifactId>mongodb-driver-sync</artifactId>  
    <version>4.9.1</version>  
</dependency>  
If not using Maven, download the JAR from MongoDB Java Driver and add it to your classpath.
Configure MongoDB connection in the application (e.g., DatabaseConnection.java):

java
Copy code
import com.mongodb.MongoClient;  
import com.mongodb.client.MongoDatabase;  

public class DatabaseConnection {  
    public static MongoDatabase getDatabase() {  
        MongoClient mongoClient = new MongoClient("localhost", 27017);  
        return mongoClient.getDatabase("contact_management");  
    }  
}  
Create the contacts collection in MongoDB:

Open the MongoDB shell or use a GUI client like MongoDB Compass:
bash
Copy code
use contact_management  
db.createCollection("contacts")  
Run the project:

Use the terminal in VS Code to compile and run:
bash
Copy code
javac Main.java  
java Main  
Directory Structure
css
Copy code
Contact-management/  
├── src/  
│   ├── Main.java  
│   ├── DatabaseConnection.java  
│   ├── Contact.java  
│   └── ContactManager.java  
├── README.md  
├── pom.xml (if using Maven)  
└── .gitignore  
Usage Instructions
Run the Program: Start the application by running Main.java.
Perform CRUD Operations: Follow the prompts to:
Add, view, update, or delete contacts.
Search for specific contacts using criteria like name.
Exit Application: Use the appropriate option to exit the program.
Contributing
Contributions are welcome! If you'd like to contribute:

Fork the repository.
Create a branch (git checkout -b feature-name).
Commit your changes (git commit -m "Add feature").
Push to your branch (git push origin feature-name).
Open a pull request.
Contact
Author: Ashwani Prajapati
Email: prajapatiashwani62@gmail.com
GitHub: Ashwani Prajapati
License
This project is licensed under the MIT License.
