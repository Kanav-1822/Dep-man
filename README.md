# ⚡ FastAPI Dependency Manager  

**FastAPI Dependency Manager** is a powerful tool that automates Python package management by allowing users to upload a `requirements.txt` file, install dependencies, and cache them in **Azure Blob Storage** for faster reuse. Built with **FastAPI**, it optimizes package retrieval, reducing redundant downloads.  

## 🚀 Features  

✅ **Automated Dependency Management** – Upload a `requirements.txt` file to install packages automatically.  
✅ **Azure Blob Storage Caching** – Reduces redundant downloads by caching dependencies.  
✅ **FastAPI-Powered API** – Lightweight, scalable, and efficient.  
✅ **Easy Integration** – Available via **pip install fastapi-dependency-manager**.  

## 📦 Installation  

```bash
pip install fastapi-dependency-manager
```
##For All the commands
```bash
dep-manager --help
```
⚙️ Usage
1️⃣ Start the FastAPI Server
```
uvicorn fastapi_dependency_manager.main:app --host 0.0.0.0 --port 8000
```
2️⃣ Upload requirements.txt and Install Dependencies
Use the API to upload your requirements.txt file and install dependencies.
API Endpoint : 
```
POST /upload-requirements
```
Example Request (cURL)
```
curl -X 'POST' 'http://localhost:8000/upload-requirements' \
-H 'Content-Type: multipart/form-data' \
-F 'file=@requirements.txt'
```
3️⃣ Retrieve Cached Dependencies
```
GET /cached-dependencies
```


🛠️ Tech Stack
*FastAPI – High-performance Python web framework
*Python – Core programming language
*Azure Blob Storage – Efficient cloud-based caching
