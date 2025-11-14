# 📄 ForgeryShield – Advanced Document Forgery Detection System

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-App-red)
![OpenCV](https://img.shields.io/badge/OpenCV-Image%20Processing-green)
![Status](https://img.shields.io/badge/Status-Active-success)

ForgeryShield is an advanced **AI-assisted document forgery detection system** built using **Streamlit**, **OpenCV**, **Pillow**, and **PyMuPDF**.  
It helps detect manipulations in documents such as certificates, government proofs, ID cards, signed letters, and any PDF-based document.

---

## ✨ Key Capabilities

### 🔍 **1. Metadata Intelligence**
Extracts and analyzes metadata to detect:
- Editing traces  
- Suspicious software signatures (Photoshop, GIMP, Adobe tools)  
- Modified timestamps  

### 🎨 **2. Error Level Analysis (ELA)**
ELA helps detect tampered regions by:
- Re-saving the image at controlled compression  
- Computing pixel-level differences  
- Highlighting altered zones with abnormal error levels  

### 🔐 **3. Template Element Verification**
Uses **OpenCV Template Matching** to verify trusted elements like:
- Signatures  
- Stamps  
- Seals  
- Logos  

Features include:
- Auto-detecting document vs. template  
- Auto-resizing template  
- Confidence scoring  

### 🧠 **4. Forgery Scoring System**
A rule-based scoring engine generates a final **PASS / FAIL** verdict.

---

## 📁 Project Directory Structure
```
ForgeryShield/
│── temp_files/                # Auto-generated cache directory
│── app.py                     # Main Streamlit application
│── requirements.txt           (Optional if you generate manually) # Dependency list
│── README.md                  # Documentation
```

---

## 🛠 Installation & Setup

### 1️⃣ Clone Repository
```bash
git clone https://github.com/yourusername/ForgeryShield.git
cd ForgeryShield
```

### 2️⃣ Install Required Libraries
If you already have a `requirements.txt`:
```bash
pip install -r requirements.txt
```

### 3️⃣ Run Application
```bash
streamlit run app.py
```

---

## 🔽 Generating requirements.txt (If not included)

Since your repository currently **does not contain a requirements.txt**, here’s the recommended way to generate one:

### ✅ **1. Generate requirements.txt from your current environment**

If all required packages are installed in your virtual environment:

#### **Command:**
```bash
pip freeze > requirements.txt
```

This creates a `requirements.txt` containing **all installed packages** in your environment.

---

## 🧪 How It Works (Technical Overview)

### ⭐ **Step 1 – PDF to Image Extraction**
- Converts the first page of a PDF to PNG using **PyMuPDF**

### ⭐ **Step 2 – Metadata Analysis**
- Examines embedded metadata  
- Flags suspicious software footprints  

### ⭐ **Step 3 – ELA Detection**
- Re-saves the image  
- Computes pixel-level differences  
- Enhances anomalies  

### ⭐ **Step 4 – Template Matching**
- Uses OpenCV's `matchTemplate`  
- Highlights regions of interest  
- Determines match confidence  

### ⭐ **Step 5 – Final Scoring**
- Combines all detection scores  
- Provides a final verdict  

---

## 📦 Dependencies

```
streamlit
opencv-python
numpy
Pillow
PyMuPDF
```

---

## 🔧 Future Enhancements

- AI-based signature verification  
- CNN-powered ELA classifier  
- Multi-page PDF support  
- Barcode/QR integrity checker  

---

## 🧑‍💻 Developed By
**Aditya SAI**  
AI & Document Forensics Enthusiast  

---

## 🤝 Contributing
Pull requests are welcome!  
Please open an issue first to discuss improvements.


