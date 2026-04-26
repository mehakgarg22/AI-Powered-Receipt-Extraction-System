# AI-Powered Receipt Extraction System

## 📌 Project Objective
A system designed to extract structured information (Store Name, Date, Total Amount) from semi-structured receipt images using OCR and NLP-based pattern matching.

## 🛠️ Tech Stack
- **Environment:** Google Colab (T4 GPU)
- **OCR Engine:** Tesseract OCR / EasyOCR
- **Image Processing:** OpenCV
- **Logic:** Python (Regex, JSON, OS)

## 🚀 How It Works
1. **Preprocessing:** Images are converted to grayscale and denoised using OpenCV to improve OCR accuracy.
2. **Text Extraction:** The system uses Tesseract to read text from diverse receipt layouts.
3. **Information Extraction:** - **Store Name:** Extracted using top-line positional logic.
   - **Date:** Identified via regex patterns (`DD/MM/YYYY`).
   - **Total Amount:** Identified using keyword-based anchoring (e.g., "Total", "Amount", "Due").
4. **Reliability:** Each field is assigned a confidence score based on OCR output and pattern validation.

## 📂 Deliverables
- `notebook.ipynb`: The complete source code.
- `results.json`: Structured output for 350+ receipt images.
- `summary.json`: A financial summary showing total spend and transaction counts.

## 📈 Challenges & Solutions
- **Noise & Blur:** Applied Fast Non-Local Means Denoising.
- **Varying Layouts:** Implemented flexible regex to catch amounts regardless of currency symbols or line position.

live link : https://colab.research.google.com/drive/1RHegfqrx3uUem6ld3xnFYzTo2LX02X5t?usp=sharing
