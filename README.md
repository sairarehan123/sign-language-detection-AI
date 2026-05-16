#  AI Sign Language Detection using Machine Learning

##  Project Overview
This project is an AI-based real-time American Sign Language (ASL) detection system that recognizes hand gestures using a webcam and converts them into readable text.

It uses **MediaPipe** for real-time hand landmark detection and a **Random Forest Machine Learning model** to classify sign language gestures into corresponding alphabets.

The system detects hand movements through a camera feed, processes hand landmarks, and predicts the sign being shown. For example, sequential gestures like **H+ E + L + L + O** can be interpreted as a word.

---

## Key Features
- Real-time hand tracking using webcam
- Detection of American Sign Language (A–Z)
- Conversion of hand gestures into alphabets
- Formation of words from sequential predictions
- Machine Learning-based classification using Random Forest
- Fast and lightweight real-time performance
- Works directly through camera input

---

##  Technologies Used
- Python
- OpenCV (for video processing)
- MediaPipe (for hand tracking and landmark detection)
- Scikit-learn (Random Forest Classifier)
- NumPy
- Pandas

---

##  Dataset Description
- Dataset consists of **American Sign Language images**
- Each alphabet class (A–Z) contains approximately **3000 images per letter**
- Only supports **American Sign Language (ASL)**

⚠️Note: Sign languages vary by region and country, so this model is specifically trained for ASL only and is not universally applicable to other sign languages.

---

## ⚙️ How the System Works
1. The webcam captures real-time video input
2. MediaPipe detects **21 hand landmarks** on the hand
3. These landmarks are extracted as numerical features
4. The trained Random Forest model (≈300 trees) processes these features
5. The model predicts the corresponding alphabet
6. The predicted output is displayed in real time
7. Sequential letters can form words (e.g., H + E + L + L + O → HELLO)

---

## Model Details
- Algorithm: Random Forest Classifier
- Number of Trees: ~300
- Input Features: 21 hand landmark coordinates (x, y, z)
- Output: Alphabet classification (A–Z)
- Task Type: Supervised Classification

---

##  Example Output
If a user performs the following gestures:

H → E → L → L → O

The system outputs:

HELLO

---

