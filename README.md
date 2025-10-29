
---

# 📄 Gemini PDF Company Extractor  
**(TR: Gemini PDF Şirket Veri Çıkarıcı)**

Gemini PDF Company Extractor is a Python tool designed to extract structured company data from multi-column, multi-page business directories in PDF format. It uses `pypdf` for text extraction and Google Gemini LLM for intelligent parsing. The output is saved as a clean CSV file, including company details and up to 30 branches per firm.

---

Gemini PDF Şirket Veri Çıkarıcı, çok sütunlu ve çok sayfalı iş rehberi PDF'lerinden yapılandırılmış şirket verisi çıkarmak için tasarlanmış bir Python aracıdır. Metin çıkarımı için `pypdf`, akıllı ayrıştırma için Google Gemini LLM kullanır. Çıktı, şirket bilgileri ve her firma için 30'a kadar şube içerecek şekilde temiz bir CSV dosyasına kaydedilir.

---

## 🚀 Features / Özellikler

- ✅ Extracts raw text from PDFs  
  (TR: PDF'den ham metin çıkarımı)
- 🤖 Parses structured data using Gemini LLM  
  (TR: Gemini LLM ile yapılandırılmış veri ayrıştırma)
- 🧠 Merges split entries across columns/pages  
  (TR: Sayfa ve sütun geçişlerinde bölünen verileri birleştirme)
- 📊 Saves output to CSV with up to 30 branches per company  
  (TR: Her şirket için 30'a kadar şube ile CSV'ye kayıt)
- 🔁 Chunked processing for long documents  
  (TR: Uzun belgeler için parça bazlı işleme)

---

## 📦 Installation / Kurulum

```bash
git clone https://github.com/kemalgunay/Gemini-PDF-Company-Extractor.git
cd Gemini-PDF-Company-Extractor
pip install -r requirements.txt
```

---

## 🔑 API Key Setup / API Anahtarı Ayarı

Set your Gemini API key as an environment variable:  
(TR: Gemini API anahtarınızı ortam değişkeni olarak ayarlayın:)

```bash
export GEMINI_API_KEY="your-api-key"
```

---

## 📁 File Structure / Dosya Yapısı

| File / Dosya | Description / Açıklama |
|--------------|------------------------|
| `main.py`    | Main extraction and CSV writing logic  
| `first_two_pages.pdf` | Sample PDF for testing  
| `extracted_company_data.csv` | Output CSV file with extracted data  

---

## ⚙️ Usage / Kullanım

```bash
python main.py
```

- Extracts text from the PDF  
  (TR: PDF'den metin çıkarılır)
- Splits text into chunks  
  (TR: Metin parçalara bölünür)
- Sends each chunk to Gemini for parsing  
  (TR: Her parça Gemini ile işlenir)
- Writes structured data to CSV  
  (TR: Yapılandırılmış veri CSV'ye yazılır)

---

## 📌 Sample Output / Örnek Çıktı

| CompanyName | Address | PhoneNumber_Main | Email | Website | CoreActivity | BranchLocation_1 | BranchPhoneNumber_1 |
|-------------|---------|------------------|-------|---------|---------------|-------------------|----------------------|
| ABC Ltd.    | London  | +44 20 1234 5678 | info@abc.com | www.abc.com | Roofing Merchant | Manchester | +44 161 987 6543 |

---

## 🧠 Notes / Notlar

- Gemini output is expected in pure JSON format  
  (TR: Gemini çıktısı saf JSON formatında beklenir)
- Missing fields are ignored during CSV writing  
  (TR: Eksik alanlar CSV yazımında atlanır)
- You can increase `MAX_BRANCHES` if needed  
  (TR: Gerekirse `MAX_BRANCHES` değeri artırılabilir)

---

## 📬 Contributing / Katkı Sağlama

Pull requests and issues are welcome!  
(TR: Pull request ve issue'lar memnuniyetle karşılanır!)

Suggestions especially appreciated for:  
(TR: Özellikle şu konularda önerilere açığız:)
- Better chunking strategies  
- Gemini prompt optimization  
- PDF layout alignment improvements

---

## 📄 License / Lisans

This project is licensed under the MIT License.  
(TR: Bu proje MIT lisansı ile lisanslanmıştır.)

---

