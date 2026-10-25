# SnapClass — AI-Powered Attendance Management System

SnapClass is an AI-powered attendance management system that combines facial recognition and voice recognition to automate classroom attendance. It helps teachers record attendance more efficiently while reducing the need for manual roll calls.

The platform allows teachers to create classes, students to enroll using QR codes, and attendance to be recorded through face and voice recognition.

## 📸 Screenshots

<!-- Add your project screenshots to the screenshots/ folder -->

### Dashboard
![SnapClass Dashboard](screenshots/dashboard.png)

### Facial Recognition Attendance
![Facial Recognition](screenshots/face_recog.png)

### Voice Recognition Attendance
![Voice Recognition](screenshots/voice_recog.png)


## ✨ Features

- **Facial Recognition:** Detects and recognizes registered students from classroom photos.
- **Voice Recognition:** Uses voice embeddings to help verify attendance through voice input.
- **QR Code Enrollment:** Allows students to join subjects using teacher-generated QR codes.
- **Automated Attendance:** Records recognized students' attendance in the database.
- **Teacher Dashboard:** Helps teachers manage subjects and attendance records.
- **Secure Authentication:** Uses Supabase Auth for user authentication.
- **Password Security:** Uses bcrypt for password hashing where passwords are handled by the application.
- **Database Security:** Uses Supabase Row-Level Security (RLS) to control access to student data.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core application logic |
| Streamlit | User interface and dashboards |
| Dlib | Face detection and facial feature processing |
| NumPy | Numerical operations on facial embeddings |
| scikit-learn | SVM-based face recognition |
| Resemblyzer | Voice embedding generation |
| Librosa | Audio processing |
| Supabase | Database, authentication, and access control |
| SQL | Database queries and attendance management |
| Segno | QR code generation |

## ⚙️ How It Works

### 1. Student Enrollment
- The teacher creates a subject and generates a QR code.
- Students scan the QR code to join the subject.
- Students register by uploading a face photo and providing a voice sample.

### 2. Facial Recognition
- The teacher uploads classroom photos containing multiple students.
- Dlib is used to detect faces.
- Facial embeddings are extracted and processed using NumPy.
- A trained SVM classifier from scikit-learn identifies registered students.

### 3. Voice Recognition
- The student provides a voice input, such as saying "present".
- Librosa helps process the audio, and Resemblyzer generates voice embeddings.
- The system compares the voice representation with registered voice data to help identify the student.

### 4. Attendance Storage
- Recognized students' attendance is recorded in Supabase.
- Teachers can review attendance records through the application.

## 🏗️ System Architecture

```text
                ┌─────────────────────┐
                │    Streamlit UI     │
                └──────────┬──────────┘
                           │
              ┌────────────┴────────────┐
              │                         │
    ┌─────────▼─────────┐    ┌──────────▼──────────┐
    │ Facial Recognition│    │ Voice Recognition   │
    │ Dlib + NumPy      │    │ Librosa + Resemblyzer│
    │ scikit-learn SVM  │    │                     │
    └─────────┬─────────┘    └──────────┬──────────┘
              │                         │
              └────────────┬────────────┘
                           │
                ┌──────────▼──────────┐
                │      Supabase       │
                │ Database + Auth +   │
                │        RLS          │
                └─────────────────────┘
```

## 🔐 Security

- Supabase Auth handles user authentication.
- Row-Level Security (RLS) policies restrict access to authorized records.
- bcrypt is used for password hashing where passwords are managed by the application.

## 🚧 Challenges and Improvements

- **Recognition accuracy:** Improved the processing of facial embeddings and vector operations to make recognition more reliable.
- **Lighting and face angles:** Recognition can be affected by poor lighting, image quality, and facial angles.
- **Background noise:** Voice recognition may become less reliable in noisy classroom environments.
- **Attendance consistency:** Debugged database and indexing-related issues to improve attendance recording.

## 👨‍💻 My Contribution

I contributed to the development of the facial recognition and voice recognition modules and the process of saving attendance records to the database.

My responsibilities included:
- Implementing facial recognition using Dlib, NumPy, and scikit-learn.
- Working on voice recognition using Resemblyzer and Librosa.
- Integrating the recognition results with the attendance database.
- Debugging recognition and attendance-recording issues.

## 🔮 Future Improvements

- Build a separate backend using FastAPI and REST APIs.
- Develop a modern frontend using React.
- Improve recognition under different lighting conditions and noisy environments.
- Add attendance analytics and downloadable reports.
- Improve scalability for larger classrooms and institutions.

## 🚀 Live Demo

**Live Application:** [SnapClass](https://snapclass-xi.vercel.app/)

## 📂 Repository

**GitHub:** [SnapClass Repository](https://github.com/arish-77/snapclass)

## 📄 License

Add a license to this repository if you intend to distribute the project under an open-source license.
