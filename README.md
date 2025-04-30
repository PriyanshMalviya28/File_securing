# 📁 Java OTP-Based File Encryption App

A console-based Java application for user registration and login via OTP (One-Time Password) sent to email. It also includes secure file hiding/unhiding functionality using a MySQL database.

---

## 🚀 Features

- ✅ User **Sign-Up** and **Login** with OTP verification  
- 🔐 OTP generated securely using random logic  
- 💾 File hiding and un-hiding with database storage  
- 📬 Email integration using **JavaMail API**  
- 🛠 MySQL-based backend storage  
- 🧩 Modular architecture (MVC-style separation)

---

1) 🗂️ Project Structure

── Main.java 
  └── Welcome.java
    ── UserView.java
  
  ├── Main.java ├── views/ │ └── Welcome.java ├── service/ │ ├── SendOTPService.java │ ├── GenerateOTP.java │ └── UserService.java ├── dao/ │ ├── UserDAO.java │ └── DataDAO.java ├── model/ │ ├── User.java │ └── Data.java ├── db/ │ └── MyConnection.java

2 )MySQL Setup

   Create a database named File_securing:
       CREATE DATABASE ytproject;
       
   Create the required tables:
      CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100) UNIQUE
);

CREATE TABLE data (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    path TEXT,
    email VARCHAR(100),
    bin_data LONGTEXT
);


3️) Email Configuration
  
  In SendOTPService.java, replace:
  
  String from = "youremail@gmail.com";
  final String password = "your-app-password";

▶️ Running the App
Open the project in IntelliJ IDEA (or your preferred IDE).

Make sure MySQL is running.

Run Main.java.

📦 Dependencies
Java 8+

MySQL 5.7+ or compatible

JavaMail API

MySQL JDBC Driver

🔐 Security Notes
Avoid hardcoding credentials in production.

Use environment variables or configuration files instead.

Email sending should use app passwords, not raw user passwords.

📄 License
MIT License

Made with ❤️ by Priyansh Malviya









   
