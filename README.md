Markdown
# 🏫 AWS-Hosted Virtual Classroom & Learning Platform

![Python](https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python)
![Flask](https://img.shields.io/badge/Flask-Backend-black?style=for-the-badge&logo=flask)
![AWS EC2](https://img.shields.io/badge/AWS%20EC2-Compute-orange?style=for-the-badge&logo=amazonec2)
![AWS S3](https://img.shields.io/badge/AWS%20S3-Storage-red?style=for-the-badge&logo=amazons3)
![AWS RDS](https://img.shields.io/badge/AWS%20RDS-Database-blue?style=for-the-badge&logo=amazonrds)
![Bootstrap](https://img.shields.io/badge/Bootstrap-Frontend-purple?style=for-the-badge&logo=bootstrap)

---

## 📌 Project Overview
This project is a **cloud-native virtual classroom web application** built using Python (Flask) and deployed on Amazon Web Services (AWS). It demonstrates the integration of core AWS services to create a secure, scalable, and responsive digital learning environment. 

Students can register, authenticate securely, and stream or download course materials, while administrators can dynamically upload and manage educational assets.

---

## 🏗️ System Architecture & Workflow

The platform leverages a classic, secure 3-tier cloud architecture:

1. **Presentation Layer:** Responsive UI built with HTML5, CSS3, JavaScript, and Bootstrap, rendered dynamically via Flask templates.
2. **Application Layer:** Flask backend hosted on an **AWS EC2** instance managing routing, session authentication, and secure AWS API communications.
3. **Storage & Data Layer:** * **AWS RDS (MySQL Engine):** Securely stores user credentials, session profiles, and file metadata.
   * **AWS S3:** A highly scalable object storage bucket utilized for hosting and serving academic PDFs, documents, and media resources via `boto3`.

---

## 🚀 Core Features & User Scenarios

### 🎓 Student Experience
* **Secure Authentication:** Self-registration and login with secure session management.
* **Interactive Dashboard:** Access to dynamically populated course catalogs.
* **Direct Content Streaming:** Fast asset downloading and previewing sourced directly from AWS S3.

### 🛠️ Administrative Control
* **Centralized Content Management:** Admin portal to upload educational materials.
* **Automated Cloud Sync:** Background scripts that upload raw files to S3 while simultaneously logging the file metadata into AWS RDS.

---

## ⚙️ Technology Stack

* **Backend:** Python, Flask, Boto3 (AWS SDK for Python), PyMySQL
* **Frontend:** HTML5, CSS3, JavaScript (ES6), Bootstrap 5
* **Cloud Infrastructure:** AWS EC2 (Compute), AWS S3 (Object Storage), AWS RDS (Managed MySQL Database)
* **Development Tools:** Git/GitHub, MySQL Workbench

---

## 📂 Project Structure

```bash
AWS-hosted-Virtual-Classroom/
│
├── Documentation/
│   └── Final document.pdf       # Detailed project report & design docs
│
├── static/                      # Custom CSS stylesheets, JS scripts, and images
│
├── templates/                   # Jinja2 HTML Templates
│   ├── home.html                # Platform landing page
│   ├── login.html               # User authentication gateway
│   ├── register.html            # New user onboarding form
│   └── courses.html             # Content repository & file download portal
│
├── app.py                       # Core Flask application & AWS initialization logic
├── requirements.txt             # Managed Python dependencies
└── README.md                    # Project documentation
🖥️ Production Deployment Guide
1. Infrastructure Setup (AWS Console)
RDS: Launch a MySQL instance, configure the security group to accept incoming traffic on port 3306 from your EC2 instance.

S3: Create a private bucket and provision an IAM user with programmatic access (AmazonS3FullAccess).

EC2: Launch an Ubuntu/Linux instance, and open ports 80 (HTTP) and 22 (SSH) in the security group.

2. Environment Configuration
SSH into your EC2 instance and configure your environment variables to secure your AWS credentials and database endpoints:

Bash
export AWS_ACCESS_KEY_ID="your_access_key"
export AWS_SECRET_ACCESS_KEY="your_secret_key"
export DB_HOST="your-rds-endpoint.amazonaws.com"
export DB_USER="admin"
export DB_PASSWORD="your_secure_password"
export DB_NAME="classroom_db"
3. Application Installation
Bash
# Clone the repository
git clone [https://github.com/yourusername/AWS-hosted-Virtual-Classroom-and-Learning-Platform.git](https://github.com/yourusername/AWS-hosted-Virtual-Classroom-and-Learning-Platform.git)
cd AWS-hosted-Virtual-Classroom-and-Learning-Platform

# Install dependencies
pip install -r requirements.txt

# Launch the server
python app.py
🖼️ Application Interfaces
## 🔗 Project Resources
* 💻 [Source Code Repository](https://github.com/spsourabh17/AWS-hosted-Virtual-Classroom-and-Learning-Platform)
* 🎥 [Watch the Full Project Demo Video](https://drive.google.com/file/d/1lljXnpmPMssLzS8PQsp_TI3S-_upUZl6/view?usp=drive_link)

---

## 👨‍💻 Author

**Sourabh Patil**

* 🔗 GitHub: [github.com/spsourabh17](https://github.com/spsourabh17)
* 💼 LinkedIn: [linkedin.com/in/sourabh-patil-5242402b7](https://www.linkedin.com/in/sourabh-patil-5242402b7)

---

## ⭐ Support
If you found this project helpful, consider giving it a ⭐ on GitHub!
