# SnapClass

SnapClass is a Streamlit-based attendance management system that uses AI-powered face and voice recognition to make classroom attendance faster and easier.

## Features

- Teacher and student login
- Subject creation and management
- Student enrollment into subjects
- Join-code based subject enrollment
- QR code sharing for subjects
- Face recognition based attendance
- Voice recognition based attendance
- Attendance history and reports
- Supabase-backed data storage

## Tech Stack

- **Python**
- **Streamlit** for the web interface
- **Supabase** for backend/database storage
- **bcrypt** for password hashing
- **NumPy** for numerical processing
- **Pandas** for attendance data handling
- **scikit-learn** for SVM-based classification
- **dlib** for face detection and face embeddings
- **face_recognition_models** for pretrained face recognition models
- **Pillow** for image processing
- **librosa** for audio processing
- **Resemblyzer** for voice embeddings and speaker recognition
- **segno** for QR code generation

## Project Structure

```text
SnapClass/
├── app.py
├── requirements.txt
├── .streamlit/
│   └── secrets.toml
└── src/
    ├── components/
    ├── database/
    ├── pipelines/
    ├── screens/
    └── ui/
