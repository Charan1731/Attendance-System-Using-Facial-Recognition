# Attendance-System-Using-Facial-Recognition
Here’s a README file template for your face recognition project using PyQt5 and OpenCV:

This project implements a face recognition-based attendance system using PyQt5, OpenCV, and SQLite. The application allows users to train a model with face data and then use it to recognize faces and log attendance records into a database.

## Features
- **Login**: Access control via password (default password: `123`).
- **Training**: Train the system with face data using OpenCV.
- **Attendance**: Record attendance by recognizing faces.
- **Reports**: View attendance reports based on the selected date.
- **Database**: Stores attendance records in an SQLite database.
- **Face Detection**: Uses Haar cascades for face detection.

## Prerequisites
- Python 3.x
- [PyQt5](https://pypi.org/project/PyQt5/)
- [OpenCV](https://pypi.org/project/opencv-python/)
- [SQLite3](https://docs.python.org/3/library/sqlite3.html)

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/face-recognition-attendance.git
   cd face-recognition-attendance
   ```

2. **Install required packages:**
   Install the necessary Python libraries using pip:
   ```bash
   pip install PyQt5 opencv-python numpy
   ```

3. **Prepare the UI file:**
   Ensure the `face.ui` file is placed in the project folder. This file contains the design for the PyQt5 interface.

4. **Database Setup:**
   When the application runs, it automatically creates the `face-reco.db` SQLite database and an `attendance` table to store the records.

## Running the Application

To run the application, execute:

```bash
python face_recognition_app.py
```

## Usage

### Login
- Enter the default password `123` to access the system.
- After successful login, the main interface appears with options for Training, Attendance, and Reports.

### Training
- Navigate to the "Training" tab.
- Enter the trainee's name and the number of face samples to be captured for training.
- Click the "Start Training" button to capture face data and store it in the `datasets` folder.

### Attendance
- Navigate to the "Attendance" tab.
- Click the "Record Attendance" button to start the face recognition process.
- If a face is recognized, attendance is automatically logged into the `attendance` table.

### Reports
- Navigate to the "Reports" tab.
- Select a date to view attendance records for that day.
- Reports are displayed in a table format with columns for ID, Name, and Date.

## File Structure

```
face-recognition-attendance/
│
├── face_recognition_app.py       # Main application code
├── face-reco.db                  # SQLite database (generated at runtime)
├── datasets/                     # Stores face data for training
├── face.ui                       # PyQt5 UI file (to be created using Qt Designer)
├── haarcascade_frontalface_default.xml  # Haarcascade XML for face detection
└── README.md                     # This file
