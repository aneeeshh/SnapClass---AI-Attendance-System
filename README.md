# 📚 SnapClass - AI Attendance System

An AI-powered attendance management system that automates student attendance using **Face Recognition** and **Voice Recognition**.

SnapClass allows teachers to create subjects, enroll students, capture classroom photos, and automatically mark attendance. Students can register, enroll in subjects, and view their attendance records through a dedicated portal.

---

## ✨ Features

- 🤖 AI-based Face Recognition
- 👥 Multiple face detection from classroom photos
- 🎙️ Voice-based attendance
- 👨‍🏫 Teacher registration and login
- 🧑‍🎓 Student registration using Face ID
- 📚 Create and manage subjects
- 📝 Student enrollment in subjects
- 📊 Attendance records and statistics
- ☁️ Supabase database integration
- 🔐 Password hashing using bcrypt
- 🖥️ Interactive Streamlit interface

---

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| 🐍 Programming Language | Python |
| 🎈 Framework | Streamlit |
| 👁️ Computer Vision | OpenCV, face_recognition |
| 🔢 Data Processing | NumPy, Pandas |
| 🧠 Machine Learning | Scikit-learn |
| 🎙️ Voice Processing | Librosa, Resemblyzer |
| ☁️ Database | Supabase |
| 🔐 Authentication | bcrypt |

---

## 🚀 How It Works

### 👨‍🏫 Teacher Portal

1. Teacher creates an account and logs in.
2. Teacher creates a subject with subject code and section.
3. Students enroll in the subject.
4. Teacher uploads classroom photos.
5. The system detects and recognizes student faces.
6. Attendance is automatically marked as **Present or Absent**.
7. Teacher can view attendance records and statistics.

### 🧑‍🎓 Student Portal

1. Student opens the Student Portal.
2. A face image is captured using the camera.
3. The system recognizes the student's face.
4. New students can register using their face.
5. Students can enroll in available subjects.
6. Students can view their attendance statistics.

---

## 👁️ Face Recognition

SnapClass uses facial embeddings to represent student faces numerically.

### 🔄 Attendance Process

**Image → Face Detection → Face Encoding → Face Matching → Student Identification → Attendance**

The system can detect multiple faces from a classroom image and identify registered students.

---

## 🎙️ Voice Attendance

SnapClass also provides a voice-based attendance option.

During registration, students can provide a short voice sample. The system generates a voice embedding using **Resemblyzer**, which can later be used for voice-based attendance.

### 🔄 Voice Attendance Process

**Voice Sample → Voice Embedding → Voice Matching → Student Identification → Attendance**

---

## ☁️ Database

SnapClass uses **Supabase** for storing application data.

### 📋 Main Database Tables

- `teachers`
- `students`
- `subjects`
- `subject_students`
- `attendance_logs`

---

## 📁 Project Structure

```text
SnapClass---AI-Attendance-System/
│
├── src/
│   ├── components/
│   │   ├── dialog_add_photo.py
│   │   ├── dialog_attendance_results.py
│   │   ├── dialog_auto_enroll.py
│   │   ├── dialog_create_subject.py
│   │   ├── dialog_enroll.py
│   │   ├── dialog_share_subject.py
│   │   ├── dialog_voice_attendance.py
│   │   ├── header.py
│   │   └── subject_card.py
│   │
│   ├── database/
│   │   ├── config.py
│   │   └── db.py
│   │
│   ├── pipelines/
│   │   ├── face_pipeline.py
│   │   └── voice_pipeline.py
│   │
│   ├── screens/
│   │   ├── home_screen.py
│   │   ├── student_screen.py
│   │   └── teacher_screen.py
│   │
│   └── ui/
│       └── base_layout.py
│
├── app.py
├── requirements.txt
├── .gitignore
└── README.md
```

---

## ⚙️ Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/aneeeshh/SnapClass---AI-Attendance-System.git
cd SnapClass---AI-Attendance-System
```

### 2️⃣ Create a Virtual Environment

```bash
python -m venv venv
```

### 3️⃣ Activate the Virtual Environment

**Windows:**

```bash
venv\Scripts\activate
```

### 4️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

> ⚠️ Some face and voice recognition dependencies may require additional setup depending on your Python version and operating system.

---

## 🔑 Supabase Configuration

Create the following file:

```text
.streamlit/secrets.toml
```

Add your Supabase credentials:

```toml
SUPABASE_URL = "your_supabase_project_url"
SUPABASE_KEY = "your_supabase_key"
```

> 🔒 **Never upload `secrets.toml` or your Supabase credentials to GitHub.**

---

## ▶️ Run the Application

Start the Streamlit application:

```bash
streamlit run app.py
```

The application will be available at:

```text
http://localhost:8501
```

---

## 🔮 Future Improvements

- 🎯 Improve face recognition accuracy
- 🎙️ Improve voice recognition reliability
- 📥 Export attendance to CSV/Excel
- 📧 Add email notifications
- 🔐 Improve authentication and authorization
- ☁️ Deploy the application to the cloud
- 🛡️ Enable database Row Level Security (RLS)
- 📊 Add advanced attendance analytics

---

## 👨‍💻 Author

**Anish Mishra**

🎓 B.Tech Computer Science & Engineering  
🤖 Aspiring Data Analyst & AI/ML Engineer

---

## 📄 License

This project is developed for **educational and portfolio purposes**.
