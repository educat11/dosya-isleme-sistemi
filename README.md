# 📁 Dosya İşleme Sistemi (Tamamen İstemci Tarafı)

Bu web uygulaması, tarayıcı içinde (GitHub Pages) çalışan hızlı bir dosya işleme aracıdır. Metin, ofis, PDF, görüntü, ses ve video dosyalarından içerik çıkarır; video/ses için konuşmayı metne çevirir; isteğe bağlı olarak metni Google Gemini ile özetler.

## 🌟 Özellikler

- **Çoklu Format Desteği**: TXT, CSV, DOCX, XLSX, PDF, MP3, WAV, OGG, M4A
- **OCR Teknolojisi**: PDF ve görsellerdeki metinleri okuma
- **Ses Tanıma**: Ses dosyalarını metne çevirme
- **Yapay Zeka Entegrasyonu**: Google Gemini API ile özetleme ve soru üretme
- **Modern Web Arayüzü**: Responsive Bootstrap tasarımı
- **Dosya İndirme**: İşlenmiş içerikleri indirme özelliği

## 🚀 Canlı Demo

🌐 **GitHub Pages Demo**: <a href="https://educat11.github.io/dosya-isleme-sistemi" target="_blank" rel="noopener noreferrer">https://educat11.github.io/dosya-isleme-sistemi</a>

## 📋 Gereksinimler

- Bir tarayıcı (Chrome/Edge önerilir)
- Google Gemini API anahtarı (kullanıcı tarafından tarayıcıya girilir ve localStorage’da saklanır)

## 🛠️ Kurulum / Geliştirme

1) Repo’yu klonlayın (opsiyonel):
```bash
git clone https://github.com/educat11/dosya-isleme-sistemi.git
cd dosya-isleme-sistemi
```
2) Geliştirme için dosyaları düzenleyip doğrudan `index.html`’i açabilirsiniz. Sunucu gerekmez.

## 🏃‍♂️ Çalıştırma

### Yerel Çalıştırma

`index.html` dosyasını çift tıklayıp tarayıcıda açmanız yeterli.

### GitHub Pages Deployment

Ana branch’e push sonrası GitHub Pages otomatik yayınlar: `https://educat11.github.io/dosya-isleme-sistemi`

## 📖 Kullanım

1. Web arayüzünden bir dosya seçin
2. Gerekirse üst kısımdan Gemini API anahtarınızı kaydedin
3. "Yükle ve İşle" deyin; ses/video otomatik transkribe edilir, metin/görsel/PDF içerikleri çıkarılır
4. İşlenmiş içerik ve (varsa) AI özeti ekranda görüntülenir ve indirilebilir

## 🔧 Teknik Detaylar

### Desteklenen Dosya Formatları

| Format | Açıklama | Özellikler |
|--------|----------|------------|
| TXT/CSV | Metin dosyaları | UTF-8/Latin-1 encoding desteği |
| DOCX | Word belgeleri | Metin + gömülü görsel OCR |
| XLSX | Excel dosyaları | Tüm sayfa verilerini çıkarma |
| PDF | PDF belgeleri | Metin + OCR + görsel işleme |
| MP3/WAV/OGG/M4A | Ses dosyaları | Doğrudan Gemini 2.5 Flash ile transkripsiyon |

### API / Kitaplıklar

- **Google Gemini**: Özetleme ve ses/metin üretimi
- **Tesseract.js**: Görsellerde OCR (tarayıcı)
- **pdf.js**: PDF metin çıkarımı (tarayıcı)
- **ffmpeg.wasm**: Videodan ses çıkarma ve MP3’e dönüştürme (tarayıcı)

## 🔒 Güvenlik Notları

- Tüm işlemler tarayıcıda yapılır; dosyalar sunucuya yüklenmez
- API anahtarınız tarayıcınızın localStorage’ında tutulur; gizliliğinizi koruyun
- Büyük videolarda tarayıcı belleği kısıtı olabilir; kısa kliplerle test edin

## 🐛 Hata Ayıklama

- "FFmpeg kütüphanesi yüklenemedi": Sayfayı yenileyin, reklam engelleyiciyi kapatın
- "Videoda ses parçası bulunamadı": Kullanılan videoda ses kanalı olmayabilir
- "API Hatası …": Geçerli Gemini API anahtarı girildiğinden emin olun

## 🤝 Katkıda Bulunma

1. Bu repository'yi fork edin
2. Yeni bir branch oluşturun (`git checkout -b feature/yeni-ozellik`)
3. Değişikliklerinizi commit edin (`git commit -am 'Yeni özellik eklendi'`)
4. Branch'inizi push edin (`git push origin feature/yeni-ozellik`)
5. Pull Request oluşturun

## 📄 Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Detaylar için `LICENSE` dosyasına bakın.

## 👨‍💻 Geliştirici

**Nail (educat11)** - [GitHub Profili](https://github.com/educat11)

## 🙏 Teşekkürler

- [Flask](https://flask.palletsprojects.com/) - Web framework
- [Google Gemini](https://ai.google.dev/) - AI API
- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) - OCR engine
- [FFmpeg](https://ffmpeg.org/) - Multimedia framework
- [Bootstrap](https://getbootstrap.com/) - CSS framework

---

⭐ Bu projeyi beğendiyseniz yıldız vermeyi unutmayın! 