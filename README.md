# \# 📚 SnapClass - AI Attendance System

# 

# SnapClass is an AI-powered attendance management system that automates student attendance using Face Recognition and Voice Recognition. The system allows teachers to create subjects, enroll students, capture classroom photos, and automatically mark attendance. Students can also register and access their enrolled subjects through a dedicated student portal.

# 

# \## ✨ Features

# 

# \- 🤖 AI-based Face Recognition for attendance

# \- 👥 Detects multiple faces from classroom photos

# \- 🎙️ Voice-based attendance option

# \- 🔐 Teacher registration and login

# \- 🧑‍🎓 Student registration using Face ID

# \- 📚 Create and manage subjects

# \- 📝 Enroll students into subjects

# \- 📊 View attendance records and statistics

# \- ☁️ Supabase database integration

# \- 🔒 Password hashing using bcrypt

# \- 🖥️ Interactive Streamlit interface

# 

# \## 🛠️ Technologies Used

# 

# \- 🐍 Python

# \- 🎈 Streamlit

# \- 👁️ OpenCV

# \- 🧠 face\_recognition

# \- 🔢 NumPy

# \- 🐼 Pandas

# \- 📈 Scikit-learn

# \- 🎵 Librosa

# \- 🎙️ Resemblyzer

# \- ☁️ Supabase

# \- 🔐 bcrypt

# 

# \## 🚀 How It Works

# 

# \### 👨‍🏫 Teacher Portal

# 

# 1\. Teacher creates an account and logs in.

# 2\. Teacher creates a subject with subject code and section.

# 3\. Students enroll in the subject.

# 4\. Teacher uploads classroom photos.

# 5\. The system detects and recognizes student faces.

# 6\. Attendance is automatically marked as Present or Absent.

# 7\. Teacher can view attendance records and statistics.

# 

# \### 🧑‍🎓 Student Portal

# 

# 1\. Student opens the Student Portal.

# 2\. A face image is captured using the camera.

# 3\. The system recognizes the student's face.

# 4\. New students can register using their face.

# 5\. Students can enroll in available subjects.

# 6\. Students can view their attendance statistics.

# 

# \## 👁️ Face Recognition

# 

# The system uses facial embeddings to represent student faces numerically.

# 

# During attendance:

# 

# 1\. 🔍 Faces are detected from the input image.

# 2\. 🧠 Facial embeddings are generated.

# 3\. 🔄 The embeddings are compared with registered student data.

# 4\. ✅ Recognized students are identified using the trained classifier.

# 5\. 📊 Attendance is recorded in the database.

# 

# \## 🎙️ Voice Attendance

# 

# SnapClass also provides a voice-based attendance option.

# 

# Students can provide a short voice sample during registration. The system generates a voice embedding using Resemblyzer and uses it for voice-based attendance.

# 

# \## ☁️ Database

# 

# The application uses Supabase as the backend database.

# 

# \### Main Database Tables

# 

# \- `teachers`

# \- `students`

# \- `subjects`

# \- `subject\_students`

# \- `attendance\_logs`

# 

# \## 📁 Project Structure

# 

# &#x20;   SnapClass---AI-Attendance-System/

# &#x20;   │

# &#x20;   ├── src/

# &#x20;   │   ├── components/

# &#x20;   │   │   ├── dialog\_add\_photo.py

# &#x20;   │   │   ├── dialog\_attendance\_results.py

# &#x20;   │   │   ├── dialog\_auto\_enroll.py

# &#x20;   │   │   ├── dialog\_create\_subject.py

# &#x20;   │   │   ├── dialog\_enroll.py

# &#x20;   │   │   ├── dialog\_share\_subject.py

# &#x20;   │   │   ├── dialog\_voice\_attendance.py

# &#x20;   │   │   ├── header.py

# &#x20;   │   │   └── subject\_card.py

# &#x20;   │   │

# &#x20;   │   ├── database/

# &#x20;   │   │   ├── config.py

# &#x20;   │   │   └── db.py

# &#x20;   │   │

# &#x20;   │   ├── pipelines/

# &#x20;   │   │   ├── face\_pipeline.py

# &#x20;   │   │   └── voice\_pipeline.py

# &#x20;   │   │

# &#x20;   │   ├── screens/

# &#x20;   │   │   ├── home\_screen.py

# &#x20;   │   │   ├── student\_screen.py

# &#x20;   │   │   └── teacher\_screen.py

# &#x20;   │   │

# &#x20;   │   └── ui/

# &#x20;   │       └── base\_layout.py

# &#x20;   │

# &#x20;   ├── app.py

# &#x20;   ├── requirements.txt

# &#x20;   ├── .gitignore

# &#x20;   └── README.md

# 

# \## ⚙️ Installation

# 

# \### 1. Clone the Repository

# 

# &#x20;   git clone https://github.com/aneeeshh/SnapClass---AI-Attendance-System.git

# &#x20;   cd SnapClass---AI-Attendance-System

# 

# \### 2. Create a Virtual Environment

# 

# &#x20;   python -m venv venv

# 

# \### 3. Activate the Virtual Environment

# 

# On Windows:

# 

# &#x20;   venv\\Scripts\\activate

# 

# \### 4. Install Dependencies

# 

# &#x20;   pip install -r requirements.txt

# 

# > ⚠️ Note: Some face and voice recognition dependencies may require additional setup depending on the Python version and operating system.

# 

# \## 🔑 Supabase Configuration

# 

# Create the following file:

# 

# &#x20;   .streamlit/secrets.toml

# 

# Add your Supabase credentials:

# 

# &#x20;   SUPABASE\_URL = "your\_supabase\_project\_url"

# &#x20;   SUPABASE\_KEY = "your\_supabase\_key"

# 

# > 🔒 Do not upload the `secrets.toml` file to GitHub.

# 

# \## ▶️ Run the Application

# 

# Start the Streamlit application:

# 

# &#x20;   streamlit run app.py

# 

# The application will open at:

# 

# &#x20;   http://localhost:8501

# 

# \## 🔮 Future Improvements

# 

# \- 🎯 Improve face recognition accuracy

# \- 🎙️ Improve voice recognition reliability

# \- 📥 Add attendance export to CSV/Excel

# \- 📧 Add email notifications for attendance

# \- 🔐 Add better authentication and authorization

# \- ☁️ Deploy the application to the cloud

# \- 🛡️ Enable database Row Level Security (RLS)

# \- 📊 Add advanced attendance analytics

# 

# \## 👨‍💻 Author

# 

# \*\*Anish Mishra\*\*

# 

# B.Tech Computer Science \& Engineering  

# Aspiring Data Analyst \& AI/ML Engineer

# 

# \## 📄 License

# 

# This project is for educational and portfolio purposes.



