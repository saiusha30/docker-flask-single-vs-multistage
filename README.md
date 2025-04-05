# 🐳 Flask Docker Build Comparison

This project demonstrates the difference between a **multi-stage Docker build** and a **single-stage (basic) Docker build** using a simple Flask web application.

Built with simplicity in mind — for learning, portfolio, and production-readiness.

## clone repositary
https://github.com/saiusha30/docker-flask-single-vs-multistage.git
cd flask-docker-build-comparison

## 📦 What’s Inside?

A clean project showing how to Dockerize the same Flask app in two ways:

| Folder             | Description                                   |
|--------------------|-----------------------------------------------|
| `with-multistage/` | Optimized build using Docker multi-stage (lean, secure, fast) |
| `without-multistage/` | Basic one-stage build (larger, less optimized)      |



## 🧱 Project Structure

lask-docker-build-comparison/ │ ├── with-multistage/ # 🚀 Clean, production-ready build │ ├── app.py │ ├── requirements.txt │ └── Dockerfile │ ├── without-multistage/ # 🧪 Simple one-layer build │ ├── app.py │ ├── requirements.txt │ └── Dockerfile │ ├── .gitignore # Ignore unnecessary files └── README.md # You're reading it!



## pre installed
docker,
git

## how to run multi stage build
cd with-multistage
docker build -t flask-multi-stage .
docker run -p 5000:5000 flask-multi-stage

Open: http://localhost:5000

## how to run single stage

cd without-multistage
docker build -t flask-single-stage .
docker run -p 5001:5000 flask-single-stage

## Multi-Stage vs Single-Stage
Feature	Multi-Stage	Single-Stage
🔐 Security	✅ High (no build tools)	❌ Lower
📦 Size	✅ ~300MB	❌ ~1.2GB
🚀 Deploy Speed	✅ Fast	❌ Slower
🛠 Build Layers	Separated cleanly	All-in-one
💼 Production Use	✅ Recommended	❌ Not Ideal

 Author
usharani parvathina



