# 🧾 PDF Invoice Data Extractor

### 📌 Overview
This Python project automatically **extracts structured invoice data** from both **selectable** and **scanned PDF invoices**, saving it into a single **Excel sheet** with proper formatting.

It combines **OCR (Optical Character Recognition)** and **regex-based text extraction** to accurately identify key invoice fields across multiple invoice templates.

---

## ⚙️ Features
✅ Extracts key details:
- **Invoice No**
- **Invoice Date**
- **Consignor Name**
- **Consignor GST**
- **Consignee Name**
- **Consignee GST**
- **HSN/SAC Code**

✅ Handles both:
- 🟢 Selectable PDFs (text-based)
- 🟡 Scanned PDFs (image-based, processed with OCR)

✅ Automatically:
- Appends data to Excel (`Extracted_Invoice_Data.xlsx`)
- Increments **Sr No**
- Supports batch processing of all PDFs in a folder

---

## 🧰 Tech Stack

| Component | Purpose |
|------------|----------|
| **Python 3.10+** | Programming language |
| **PyPDF2** | Extract text from selectable PDFs |
| **pdf2image** | Convert scanned PDFs to images |
| **pytesseract** | OCR engine for text extraction |
| **pandas** | Data handling and Excel writing |
| **openpyxl** | Excel writer |
| **Pillow (PIL)** | Image processing |

---

## 📦 Installation

### 1️⃣ Clone or Copy This Repository
```bash
git clone https://github.com/<your-username>/pdf-invoice-extractor.git
cd pdf-invoice-extractor
````

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Install External Tools

#### 🧩 **Poppler for Windows**

* Download: [https://github.com/oschwartz10612/poppler-windows/releases](https://github.com/oschwartz10612/poppler-windows/releases)
* Extract to:
  `C:\Program Files\poppler-25.07.0\Library\bin`
* Add this path to your **System Environment Variables → PATH**

#### 🔠 **Tesseract OCR**

* Download: [https://github.com/UB-Mannheim/tesseract/wiki](https://github.com/UB-Mannheim/tesseract/wiki)
* Default install path:
  `C:\Program Files\Tesseract-OCR`
* Add this path to your **System Environment Variables → PATH**

---

## 📂 Project Structure

```
pdf-invoice-extractor/
│
├── Extract_Invoice_Data.py        # Main extraction script
├── requirements.txt               # Python dependencies
├── Extracted_Invoice_Data.xlsx    # Output Excel file (auto-created)
├── Caterpillar -Invoice.pdf       # Sample selectable invoice
├── Sawan.pdf                      # Sample scanned invoice
└── README.md                      # Project documentation
```

---

## 🚀 Usage

1. Place all your **invoice PDFs** inside the project folder.

2. Run the Python script:

   ```bash
   python Extract_Invoice_Data.py
   ```

3. The script will:

   * Process every `.pdf` file in the folder
   * Use **OCR** automatically for scanned files
   * Append extracted details to `Extracted_Invoice_Data.xlsx`

---

## 📊 Example Output

| Sr No | Invoice No      | Invoice Date | Consignor Name                                | Consignor GST   | Consignee Name                                  | Consignee GST   | HSN/SAC Code |
| ----- | --------------- | ------------ | --------------------------------------------- | --------------- | ----------------------------------------------- | --------------- | ------------ |
| 1     | BOSAMD25060069  | 19-Jun-2025  | Caterpillar Cargo Solutions (India) Pvt. Ltd. | 24AAECC1386Q1ZA | Larsen & Toubro Limited, L&T Energy Hydrocarbon | 06AAACL0140P9ZF | 996531       |
| 2     | SEPL/1125/24-25 | 25/02/2025   | Sawan Engineers Pvt. Ltd.                     | 24AAKCS9876P1Z7 | Larsen & Toubro Limited, L&T Energy Hydrocarbon | 18AAACL0140P7ZC | 73079390     |

---

## 🧠 Notes

* If **Tesseract** or **Poppler** are not found in the system path, OCR will not work.
* Use **high-quality scanned PDFs (300 DPI or higher)** for better OCR accuracy.
* You can tweak regex patterns in the script to adapt to different invoice formats.

---

## 👨‍💻 Author

**Aavishkar Kedari**
*Data Scientist • Generative AI Enthusiast*

📧 [aavishkarkedari@gmail.com](mailto:aavishkarkedari@gmail.com)
🌐 [GitHub Profile](https://github.com/<your-username>)

---

## 🪪 License

This project is open-source and available under the **MIT License**.
Feel free to use and modify it for personal or commercial projects.

````

Would you like me to also generate a **`requirements.txt`** file content that fits perfectly with this README (for direct inclusion in your repo)?
