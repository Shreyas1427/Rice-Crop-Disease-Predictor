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
Dockerize_API/
├── main.py                 # FastAPI code for the application
├── requirements.txt        # Python dependencies
├── Dockerfile              # Dockerfile for containerization
├── static/                 # Folder for static assets (e.g., CSS, images)
├── templates/              # HTML templates for the frontend
├── .github/
│   └── workflows/
│       └── cicd.yml        # GitHub Actions pipeline
├── README.md               # Project documentation
