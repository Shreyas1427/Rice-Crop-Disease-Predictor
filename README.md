# Rice-Crop-Disease-Predictor

A FastAPI-based project for rice disease prediction using a TensorFlow model. This repository includes containerization with Docker and a CI/CD pipeline using GitHub Actions.

---

## 🚀 Features
- **FastAPI**: An efficient backend API for image-based predictions.
- **Pre-trained Model**: Predicts rice diseases using a TensorFlow model.
- **Dockerized Deployment**: Runs seamlessly in any Docker-compatible environment.
- **CI/CD Integration**: Automates testing, building, and deployment using GitHub Actions.

---

## 📂 Project Structure

```plaintext
Rice-Crop-Disease-Predictor/
├── main.py                 # FastAPI code for the application
├── requirements.txt        # Python dependencies
├── Dockerfile              # Dockerfile for containerization
├── static/                 # Folder for static assets (e.g., CSS, images)
├── templates/              # HTML templates for the frontend
├── .github/
│   └── workflows/
│       └── cicd.yml        # GitHub Actions pipeline
├── README.md               # Project documentation
```

## 🛠️ Setup Instructions
```
1. Clone the Repository
git clone https://github.com/<your-username>/Rice-Crop-Disease-Predictor.git
cd Rice-Crop-Disease-Predictor

2. Build and Run the Docker Container
docker build -t dockerize_api .
docker run -d -p 8000:8000 dockerize_api
This will expose the FastAPI app on port 8000. Access it via http://localhost:8000.

3.Configure an AWS EC2 Instance
a.Launch an EC2 instance:
 Choose an Amazon Linux 2 or Ubuntu AMI.
 Select an instance type (e.g., t2.micro for free tier).
 Configure security group rules to allow:
 Port 22 (SSH)
 Port 8000 (application access)
 Download the private key file (e.g., api.pem).

b.Connect to the EC2 instance:
 ssh -i "api.pem" ec2-user@<EC2-Public-IP

c.Install Docker on EC2:
 sudo yum update -y
 sudo yum install docker -y
 sudo service docker start
 sudo usermod -a -G docker ec2-user
 logout
 Reconnect to apply changes.

4.Deploy the Docker Container on EC2
a.Pull the Docker image from Docker Hub:
docker pull <your-dockerhub-username>/dockerize_api:v1.0
b.Run the container:
docker run -d -p 8000:8000 <your-dockerhub-username>/dockerize_api:v1.0
c.Verify the application:
Open a browser and navigate to http://<EC2-Public-IP>:8000.
```


## 🔄 CI/CD Pipeline
The project includes a GitHub Actions CI/CD workflow that automates the following processes:
Building the Docker image for the FastAPI application.
Pushing the image to Docker Hub (shreyas721/rdp:v1.0).
Deploying the container to an EC2 instance.
Important: Before deploying, ensure your EC2 instance is set up to accept Docker images and the docker service is running.

## 🧰 Technologies Used
FastAPI: Web framework for Python.
Docker: Containerization for easy deployment.
GitHub Actions: CI/CD automation.
TensorFlow: Machine Learning model for predictions.
AWS EC2

## 👨‍💻 Authors
Sudhanshu Dave
Sharvari Hendre
Shreyas Kempwade
Ashutosh Korde
