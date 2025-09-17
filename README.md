# 🎭 Photo to Emoji – Real-Time Emotion Detection

A Python project that detects facial emotions in real-time using a webcam feed and displays corresponding emojis.  
Built with **OpenCV**, **Keras (CNN)**, **Tkinter GUI**, and **ImageDataGenerator**.

---

## 📸 Features
- Real-time face detection using Haar Cascades.
- Emotion recognition using a trained CNN model (`model.h5`).
- Displays corresponding emojis alongside the webcam feed.
- Tkinter-based GUI with live updates.


---

## 🗂️ Project Structure  

```
emoji-creator/
│
├── data/
│   ├── train/                # Training images organized in class subfolders
│   └── test/                 # Validation images organized in class subfolders
│
├── emojis/                   # Emoji images for each emotion
│   ├── angry.png
│   ├── disgusted.png
│   ├── fearful.png
│   ├── happy.png
│   ├── neutral.png
│   ├── sad.png
│   └── surprised.png
│
├── model.h5                  # Trained Keras model weights
├── logo.png                  # App logo
├── requirements.txt          # Python dependencies
├── main.py                   # Tkinter + OpenCV app entry point
└── README.md                 # Project documentation (this file)
```

---
## 🛠 Requirements

Install the following packages:

```bash
pip install numpy opencv-python keras tensorflow pillow
```

> **Note:**  
> Use Python 3.8+ for compatibility with TensorFlow/Keras.

---

## 🚀 How to Run

### 1️⃣ Clone the repository

```bash
git clone https://github.com/Aditya123589/emoji-creator.git
cd photo-to-emoji
```

### 2️⃣ Train the Model (Optional)

If you want to train from scratch:

```bash
python train_model.py
```

This will create/update `emotion_model.h5`.

### 3️⃣ Run the Application

```bash
python emotion_app.py
```

Tkinter GUI will open and start showing:
- Live webcam feed with detected faces.
- Predicted emotion label.
- Corresponding emoji image.

---

## 🤖 Model Details

- **Architecture:** 4 Convolutional Layers + MaxPooling + Dense layers.
- **Input:** 48x48 grayscale facial images.
- **Output:** 7 Emotion Classes
  - Angry
  - Disgusted
  - Fearful
  - Happy
  - Neutral
  - Sad
  - Surprised

---

## 📝 Customization

- To add more emojis: place new images in `emojis/` and update the `emoji_dist` dictionary.
- To change the face detector, replace the Haar Cascade path with your custom `.xml`.



## 💡 Future Improvements
- Deploy as a Streamlit or Flask web app.
- Add more emotion categories.
- Improve accuracy with a deeper CNN or transfer learning (e.g., MobileNet).

---

## 👨‍💻 Author

- **Your Name** – [GitHub](https://github.com/Aditya123589)

---

⭐ **If you like this project, don’t forget to give it a star!**
