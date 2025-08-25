# 📁 Dosya İşleme Sistemi

Bu sistem, çeşitli dosya formatlarını (TXT, CSV, DOCX, XLSX, PDF, MP3, WAV, OGG, M4A) işleyebilen ve içeriklerini çıkarabilen bir web uygulamasıdır. Ayrıca metin dosyaları için yapay zeka ile özet ve soru üretme özelliği bulunmaktadır.

## 🌟 Özellikler

- **Çoklu Format Desteği**: TXT, CSV, DOCX, XLSX, PDF, MP3, WAV, OGG, M4A
- **OCR Teknolojisi**: PDF ve görsellerdeki metinleri okuma
- **Ses Tanıma**: Ses dosyalarını metne çevirme
- **Yapay Zeka Entegrasyonu**: Google Gemini API ile özetleme ve soru üretme
- **Modern Web Arayüzü**: Responsive Bootstrap tasarımı
- **Dosya İndirme**: İşlenmiş içerikleri indirme özelliği

## 🚀 Canlı Demo

🌐 **GitHub Pages Demo**: [https://yourusername.github.io/dosya-isleme-sistemi](https://yourusername.github.io/dosya-isleme-sistemi)

## 📋 Gereksinimler

- Python 3.8 veya üzeri
- Tesseract OCR
- FFmpeg
- Google Gemini API anahtarı

## 🛠️ Kurulum

### Yerel Kurulum

1. **Repository'yi klonlayın:**
```bash
git clone https://github.com/yourusername/dosya-isleme-sistemi.git
cd dosya-isleme-sistemi
```

2. **Gerekli sistem paketlerini yükleyin:**

```bash
# Ubuntu/Debian için:
sudo apt update
sudo apt-get install -y tesseract-ocr tesseract-ocr-tur
sudo apt-get install -y ffmpeg
sudo apt-get install -y poppler-utils

# Windows için:
# Tesseract OCR: https://github.com/UB-Mannheim/tesseract/wiki
# FFmpeg: https://ffmpeg.org/download.html
```

3. **Python paketlerini yükleyin:**

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# veya
venv\Scripts\activate     # Windows
pip install -r requirements.txt
```

4. **Google Gemini API anahtarınızı ayarlayın:**
   - `13_2.py` dosyasında `GEMINI_API_KEY` değişkenini kendi API anahtarınızla güncelleyin.

## 🏃‍♂️ Çalıştırma

### Yerel Çalıştırma

```bash
python 13_2.py
```

Tarayıcınızda `http://localhost:5000` adresine gidin.

### GitHub Pages Deployment

Bu proje GitHub Actions ile otomatik olarak deploy edilir. Ana branch'e push yaptığınızda otomatik olarak GitHub Pages'te yayınlanır.

## 📖 Kullanım

1. Web arayüzünden bir dosya seçin
2. "Yükle ve İşle" butonuna tıklayın
3. İşlem tamamlandığında:
   - İşlenmiş içeriği görüntüleyebilirsiniz
   - İşlenmiş dosyayı indirebilirsiniz
   - Metin dosyaları için yapay zeka özetini görüntüleyebilir ve indirebilirsiniz

## 🔧 Teknik Detaylar

### Desteklenen Dosya Formatları

| Format | Açıklama | Özellikler |
|--------|----------|------------|
| TXT/CSV | Metin dosyaları | UTF-8/Latin-1 encoding desteği |
| DOCX | Word belgeleri | Metin + gömülü görsel OCR |
| XLSX | Excel dosyaları | Tüm sayfa verilerini çıkarma |
| PDF | PDF belgeleri | Metin + OCR + görsel işleme |
| MP3/WAV/OGG/M4A | Ses dosyaları | Google Speech Recognition |

### API Entegrasyonu

- **Google Gemini API**: Metin özetleme ve soru üretme
- **Google Speech Recognition**: Ses dosyası işleme
- **Tesseract OCR**: Görsel metin tanıma

## 🔒 Güvenlik Notları

- Uygulama varsayılan olarak tüm IP adreslerinden erişime açıktır (`0.0.0.0`)
- Üretim ortamında bir reverse proxy (örn. Nginx) ve SSL sertifikası kullanmanız önerilir
- Maksimum dosya boyutu 16MB ile sınırlıdır
- API anahtarlarını güvenli bir şekilde saklayın

## 🐛 Hata Ayıklama

### Yaygın Sorunlar

- **Tesseract OCR hataları**: `tesseract --version` komutu ile kurulumu kontrol edin
- **FFmpeg hataları**: `ffmpeg -version` komutu ile kurulumu kontrol edin
- **Dosya izinleri**: `uploads` klasörünün yazma izinlerini kontrol edin
- **API anahtarı hataları**: Gemini API anahtarının geçerli olduğunu kontrol edin

### Log Dosyaları

Uygulama çalışırken konsol çıktısında detaylı log bilgileri görüntülenir.

## 🤝 Katkıda Bulunma

1. Bu repository'yi fork edin
2. Yeni bir branch oluşturun (`git checkout -b feature/yeni-ozellik`)
3. Değişikliklerinizi commit edin (`git commit -am 'Yeni özellik eklendi'`)
4. Branch'inizi push edin (`git push origin feature/yeni-ozellik`)
5. Pull Request oluşturun

## 📄 Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Detaylar için `LICENSE` dosyasına bakın.

## 👨‍💻 Geliştirici

**Nail** - [GitHub Profili](https://github.com/yourusername)

## 🙏 Teşekkürler

- [Flask](https://flask.palletsprojects.com/) - Web framework
- [Google Gemini](https://ai.google.dev/) - AI API
- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) - OCR engine
- [FFmpeg](https://ffmpeg.org/) - Multimedia framework
- [Bootstrap](https://getbootstrap.com/) - CSS framework

---

⭐ Bu projeyi beğendiyseniz yıldız vermeyi unutmayın! 