# EmailJS Test Rehberi

## 🚀 Hızlı Test Adımları

### 1. Yerel Sunucu Başlatma
```bash
# Python 3 ile
python -m http.server 8000

# Python 2 ile (eski sistemler)
python -m SimpleHTTPServer 8000

# Node.js varsa
npx serve .
```

### 2. Tarayıcıda Test
- `http://localhost:8000` adresine gidin
- İletişim formuna gidin
- Test verisi girin

## 🧪 Test Verileri Örnekleri

### Test Formu:
```
Ad Soyad: Test Kullanıcı
E-posta: test@example.com (kendi e-postanızı kullanın)
Hizmet: Üniversite Seçimi
Mesaj: Bu bir test mesajıdır.
```

## 🔍 Hata Ayıklama

### Console Kontrol (F12):
1. Tarayıcıda F12 tuşuna basın
2. Console sekmesine gidin
3. Hata mesajlarını kontrol edin

### Yaygın Hatalar:

#### ❌ "EmailJS is not defined"
**Sebep:** Script yüklenmemiş
**Çözüm:** İnternet bağlantınızı kontrol edin

#### ❌ "Invalid service ID"
**Sebep:** Yanlış service ID
**Çözüm:** EmailJS dashboard'dan doğru ID'yi kopyalayın

#### ❌ "Template not found"
**Sebep:** Yanlış template ID
**Çözüm:** EmailJS'de template oluşturun ve ID'yi güncelleyin

#### ❌ "Public key is invalid"
**Sebep:** Yanlış public key
**Çözüm:** EmailJS account settings'den doğru key'i alın

## ✅ Başarı Kontrolleri

### 1. Form Gönderimi
- "Gönderiliyor..." yazısı görünmeli
- Yeşil başarı bildirimi çıkmalı
- Form temizlenmeli

### 2. E-posta Kontrolü
- EmailJS'e bağladığınız e-postanızı kontrol edin
- Spam klasörünü de kontrol edin
- 1-2 dakika bekleyin

### 3. EmailJS Dashboard
- EmailJS dashboard'a gidin
- "Logs" sekmesini kontrol edin
- Gönderilen e-postaları görebilirsiniz

## 🌐 Alternatif Test Yöntemleri

### 1. GitHub Pages (Ücretsiz)
```bash
# GitHub'a yükle
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin [repo-url]
git push -u origin main

# Settings > Pages > Source: main branch
```

### 2. Netlify Drop (Anında)
- netlify.com/drop adresine gidin
- Proje klasörünüzü sürükleyin
- Anında canlı link alın

### 3. Vercel (Hızlı)
- vercel.com'a gidin
- Projeyi yükleyin
- Otomatik deploy

## 📱 Mobil Test

### Chrome DevTools:
1. F12 tuşuna basın
2. Device toolbar'ı açın (Ctrl+Shift+M)
3. Farklı cihazları test edin

### Gerçek Cihaz:
1. Bilgisayarınızın IP adresini bulun (ipconfig)
2. Telefonda `http://[IP]:8000` adresine gidin

## 🔧 Debug Modu

Test için debug bilgilerini görmek isterseniz, script.js'e ekleyin:

```javascript
// Form gönderimi öncesi debug
console.log('Form data:', data);
console.log('Service ID:', 'service_pgdk826');
console.log('Template ID:', 'template_yse10j5');

// EmailJS yanıtı
.then(function(response) {
    console.log('EmailJS Success:', response);
    // ... rest of code
})
.catch(function(error) {
    console.log('EmailJS Error:', error);
    // ... rest of code
});
``` 