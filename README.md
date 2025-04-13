# 🧠 Brain Tumor Detection using CNN

This project is a **Brain Tumor Detection System** that uses **Convolutional Neural Networks (CNN)** to classify MRI scans as either **"Tumor Detected"** or **"No Tumor"**. It features an intuitive **Streamlit web interface** for real-time predictions.

---

## 📌 Project Overview

- **Model**: CNN-based image classifier
- **Dataset**: Brain MRI Images (`yes` and `no` folders)
- **Interface**: Streamlit Web App with ngrok tunneling
- **Libraries**: TensorFlow, OpenCV, NumPy, Matplotlib, Streamlit

---

## 🚀 Features

✅ Load and preprocess MRI scans  
✅ Resize all images to `150x150`  
✅ Normalize and split into train/test  
✅ CNN model with Conv2D, MaxPooling, and Dropout  
✅ Achieved **84.31% Validation Accuracy**  
✅ Deployed via **Streamlit + ngrok** for remote access  
✅ Real-time image classification with confidence score  

---

## 🧪 Model Architecture

- `Conv2D(32)` + `MaxPooling2D`
- `Conv2D(64)` + `MaxPooling2D`
- `Conv2D(128)` + `MaxPooling2D`
- `Flatten` + `Dense(128)` + `Dropout(0.5)`
- `Output`: `Dense(1, sigmoid)` for binary classification

---

## 📊 Model Performance

| Metric         | Score     |
|----------------|-----------|
| **Accuracy**   | 84.31%    |
| **Loss**       | 0.456     |
| **Epochs**     | 10        |
| **Input Size** | 150x150   |

---

## 🖼️ Sample Output

| Uploaded MRI Image | Prediction       | Confidence     |
|--------------------|------------------|----------------|
| ![Sample MRI](https://via.placeholder.com/150) | Tumor Detected | 0.84 |
| ![Sample MRI](https://via.placeholder.com/150) | No Tumor        | 0.22 |

---

## ⚙️ How to Run

### 1️⃣ Clone the repo and install dependencies

```bash
pip install tensorflow opencv-python numpy matplotlib streamlit pyngrok


2️⃣ Train & Save the Model (if needed)
Model is saved as brain_tumor_model.h5.

3️⃣ Run the Streamlit App

streamlit run app.py


4️⃣ Expose via ngrok

ngrok config add-authtoken <YOUR_AUTH_TOKEN>
ngrok http 8501


📂 Dataset Details

Source: Kaggle Brain Tumor Dataset

Classes: yes (tumor), no (no tumor)

Image Count: ~3000

Resolution: Original 256x256 (resized to 150x150)


🔧 Future Improvements


 Add Data Augmentation

 Hyperparameter Tuning

 Convert to Mobile App using TensorFlow Lite

 Add Grad-CAM Visualizations

📄 License

This project is licensed under the MIT License.

🤝 Contact & Contributions


Contributions are welcome! Submit PRs or raise issues.
📬 Reach me at: chintanchhajed@gmail.com
