# Deploy Bus Booking Application on AWS-12

## 📌 Project Overview

This project demonstrates how to deploy a real-world Bus Booking Application on AWS using Amazon EC2, Amazon RDS, and Elastic Load Balancer.

The main objective of this project is to host a scalable and reliable web application in the cloud environment. The application uses EC2 instances for hosting, RDS for database management, and Load Balancer for distributing traffic efficiently.

This project helps in understanding real-world AWS deployment architecture and cloud-based application hosting.

---

# 🎯 Objective

* Deploy real-world web application
* Host scalable cloud infrastructure
* Configure database connectivity
* Improve application availability
* Distribute traffic using Load Balancer
* Understand cloud deployment workflow

---

# 🧰 AWS Services Used

## 1. Amazon EC2

Used to host the Bus Booking Application.

## 2. Amazon RDS

Used to manage the backend relational database.

## 3. Elastic Load Balancer (ELB)

Used to distribute incoming traffic across multiple EC2 instances.

## 4. Security Groups

Used to securely manage inbound and outbound traffic.

## 5. AWS VPC

Provides secure networking environment.

## 6. IAM Roles

Used to securely manage AWS permissions.

---

# 🏗️ Project Architecture

The project architecture includes:

1. Launching EC2 Instances
2. Installing Application Dependencies
3. Configuring RDS Database
4. Connecting Application with Database
5. Creating Load Balancer
6. Configuring Security Groups
7. Deploying Bus Booking Application
8. Testing Application Accessibility

---

# ⚙️ Project Folder Structure

```bash
12. Deploy Bus Booking Application/
│
├── app/
│   ├── templates/
│   ├── static/
│   ├── app.py
│   └── requirements.txt
│
├── database/
│   └── database_setup.sql
│
├── deployment/
│   ├── install_dependencies.sh
│   ├── configure_server.sh
│   └── run_application.sh
│
├── images/
│
└── README.md
```

---

# ⚙️ Step-by-Step Implementation

## Step 1: Launch EC2 Instance

* Open AWS Console
* Go to EC2 Dashboard
* Click Launch Instance
* Select Amazon Linux or Ubuntu AMI
* Choose Instance Type
* Configure Security Group
* Allow:

  * HTTP (Port 80)
  * SSH (Port 22)

---

## Step 2: Connect to EC2 Instance

Use SSH to connect:

```bash
ssh -i key.pem ec2-user@your-public-ip
```

---

## Step 3: Install Application Dependencies

Install required packages:

```bash
sudo yum update -y
sudo yum install python3 -y
pip3 install -r requirements.txt
```

---

## Step 4: Configure Amazon RDS

* Create RDS Database
* Choose MySQL or PostgreSQL
* Configure username and password
* Allow database access from EC2

---

## Step 5: Connect Application with RDS

Update database configuration inside application:

```python
DB_HOST = 'your-rds-endpoint'
DB_USER = 'admin'
DB_PASSWORD = 'password'
DB_NAME = 'busbookingdb'
```

---

## Step 6: Create Load Balancer

* Go to EC2 Dashboard
* Select Load Balancers
* Create Application Load Balancer
* Configure Listener:

  * HTTP : 80
* Attach EC2 instances

---

## Step 7: Deploy Application

Run application server:

```bash
python3 app.py
```

Verify application deployment in browser.

---

## Step 8: Test Application

* Copy Load Balancer DNS URL
* Open in browser
* Verify Bus Booking Application loads successfully
* Test booking features

---

# 📸 Project Screenshots

## 🔹 EC2 Instance Setup

<img width="1051" height="452" alt="Instances" src="https://github.com/user-attachments/assets/c5cab8f9-4fe2-46b1-a00d-6da839fe7f73" />

---

## 🔹 Target Group

<img width="1060" height="445" alt="Target Groups" src="https://github.com/user-attachments/assets/7be7feb8-9f7e-4c64-93cc-a92c954799ec" />

---

## 🔹 Security Group Configuration

<img width="1052" height="439" alt="Security Groups" src="https://github.com/user-attachments/assets/19ec86e0-6f2a-4d55-a427-a4f2f40afc90" />

---

## 🔹 Final Output
<img width="1014" height="245" alt="Output-DNS" src="https://github.com/user-attachments/assets/89e71c3d-d17e-4de7-9723-a984eb9b2fd6" />

<img width="941" height="280" alt="Output-IP" src="https://github.com/user-attachments/assets/d6262d4d-3eb5-4907-9907-032eabc404e5" />

---

# ✅ Features

* Real-world Application Deployment
* Database Integration using RDS
* Scalable Infrastructure
* Load Balanced Traffic Distribution
* Secure Cloud Deployment
* High Availability
* Centralized Database Management

---

# 📚 Learning Outcomes

Through this project, I learned:

* How to deploy real-world applications on AWS
* How Amazon RDS works
* How Load Balancer distributes traffic
* How to connect applications with databases
* Security Group configuration
* Cloud application deployment process
* AWS infrastructure management

---

# 🚀 Future Improvements

* Add HTTPS Support
* Configure Auto Scaling
* Add CloudWatch Monitoring
* Implement CI/CD Pipeline
* Add User Authentication
* Improve Database Security

---

# 🏁 Conclusion

This project successfully demonstrates deployment of a Bus Booking Application on AWS using EC2, RDS, and Load Balancer. The infrastructure provides scalable, secure, and reliable cloud hosting for real-world web applications.

---

# 👩‍💻 Author

Akshata Naik

---
