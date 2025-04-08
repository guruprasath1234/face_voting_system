# 🗳️ Smart Face Recognition Voting System

A secure, AI-powered face recognition-based voting system built with Python and OpenCV. This system ensures that only authorized users can vote and that each person can vote only once using real-time face detection and recognition.

---

## 🤖 How It Works

### 1. Face Registration (`add_faces.py`)
- The system captures 51 facial images using your webcam.
- Each voter is uniquely identified by their Aadhar number.
- Facial data and names are stored using `pickle` in the `data/` directory.

### 2. Face Recognition and Voting (`give_vote.py`)
- When the voting script is run, the webcam scans for a registered face.
- Once the face is recognized:
  - If the voter **has not voted yet**, they are allowed to cast a vote using the keyboard.
  - If the voter **has already voted**, the system blocks duplicate voting with a warning.
- Votes are saved in `Votes.csv` with name, vote, date, and time.
- The system uses the Windows speech API to give voice feedback.

---

## 🛠️ How to Run

### Step 1: Install Dependencies
Make sure Python is installed on your system, then install the required libraries:

```bash
pip install -r requirements.txt
