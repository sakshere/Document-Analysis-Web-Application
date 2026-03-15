# 📄 Document Analysis Web Application

## Overview
The **Document Analysis Web Application** allows users to upload scanned PDFs and extract text-based insights using **Tesseract.js OCR**. The application provides various document statistics and word frequency analysis in a user-friendly interface.

## 🛠 Features
### ✅ Frontend:
- **Drag-and-drop file upload** (Supports PDF and images)
- **Document statistics**:
  - Word count
  - Character count (with and without spaces)
  - Sentence count
  - Average word length
- **Word frequency analysis**:
  - Top 20 most frequent words
  - Option to exclude common words (stop words)
- **Loading states & error handling**
- **Responsive UI** (Mobile & desktop-friendly)

### ✅ Backend:
- **File validation** (Ensures only PDFs and images are uploaded)
- **Tesseract.js Integration** (OCR for text extraction)
- **Text analysis computation** (Statistics & word frequency)
- **RESTful API endpoints** with proper error handling

## 📂 Repository Structure
```
Document_Analysis_Web_Application/
│── backend/               # Node.js backend with Tesseract.js OCR
│── frontend/              # React frontend for UI
│── public/                # Static assets
│── src/                   # Frontend components
│── .gitignore
│── README.md
│── package.json
│── server.js              # Main backend server file
```

## 🛠️ Setup Instructions
### **1️⃣ Clone the Repository**
```sh
git clone https://github.com/sakshere/Document-Analysis-Web-Application.git
cd Document_Analysis_Web_Application
```

### **2️⃣ Install Dependencies**
#### **Backend:**
```sh
cd backend
npm install
```
#### **Frontend:**
```sh
cd frontend
npm install
```

### **3️⃣ Setup Environment Variables**
Create a **.env** file in the `backend` directory and add the following:
```
PORT=5000
```

### **4️⃣ Run the Application**
#### **Start Backend:**
```sh
cd backend
npm start
```
#### **Start Frontend:**
```sh
cd frontend
npm start
```

## 🔗 API Endpoints
| Method | Endpoint          | Description |
|--------|------------------|-------------|
| POST   | `/upload`        | Uploads a document and extracts text |
| GET    | `/analysis`      | Returns text statistics & word frequency |

## ⚖️ Design Decisions & Trade-offs
- **Tesseract.js** was chosen for **client-side OCR processing**.
- **In-memory processing** instead of database storage to keep it lightweight.
- **Handles both PDFs and images** for OCR.
- **No authentication** as this is a standalone document analysis tool.

## Future Improvements
- ✅ Support for **multi-file upload**
- ✅ **Downloadable reports** (PDF/CSV)
- ✅ **Advanced NLP analysis** (Sentiment, named entity recognition)
- ✅ **User authentication & history tracking**



