# EmailJS Kurulum Rehberi

## 1. EmailJS Hesabı Oluşturma

1. [EmailJS.com](https://www.emailjs.com/) adresine gidin
2. "Sign Up" butonuna tıklayın
3. Ücretsiz hesap oluşturun (ayda 200 e-posta limiti)

## 2. E-posta Servisi Ekleme

1. Dashboard'da "Email Services" sekmesine gidin
2. "Add New Service" butonuna tıklayın
3. Gmail, Outlook, Yahoo vb. seçin
4. E-posta hesabınızı bağlayın

## 3. E-posta Template Oluşturma

1. "Email Templates" sekmesine gidin
2. "Create New Template" butonuna tıklayın
3. Aşağıdaki template'i kullanın:

### Template İçeriği:
```
Konu: Yeni İletişim Formu Mesajı - {{from_name}}

Gönderen: {{from_name}}
E-posta: {{from_email}}
İlgilenilen Hizmet: {{service}}

Mesaj:
{{message}}

---
Bu mesaj Road2Germany web sitesinden gönderilmiştir.
```
-
## 4. Kodda Güncellemeler

### index.html dosyasında:
```javascript
// Bu satırı bulun:
emailjs.init('YOUR_PUBLIC_KEY');

// YOUR_PUBLIC_KEY'i EmailJS hesabınızdan aldığınız Public Key ile değiştirin
emailjs.init('user_xxxxxxxxxx');
```

### script.js dosyasında:
```javascript
// Bu satırları bulun:
emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', {

// YOUR_SERVICE_ID ve YOUR_TEMPLATE_ID'yi EmailJS'den aldığınız değerlerle değiştirin
emailjs.send('service_xxxxxxx', 'template_xxxxxxx', {
```

## 5. Test Etme

1. Web sitenizi açın
2. İletişim formunu doldurun
3. "Mesaj Gönder" butonuna tıklayın
4. E-posta kutunuzu kontrol edin

## Alternatif Seçenekler

### Seçenek 1: WhatsApp Entegrasyonu
script.js dosyasında WhatsApp seçeneğini aktif etmek için:
1. EmailJS kodunu yorum satırına alın (/* */)
2. WhatsApp kodunun yorum satırlarını kaldırın
3. WhatsApp numaranızı güncelleyin

### Seçenek 2: Local Storage (Geliştirme için)
- Basit test amaçlı
- Mesajlar tarayıcının Local Storage'ında saklanır
- F12 > Console'da mesajları görebilirsiniz

## Güvenlik Notları

- Public Key'inizi kimseyle paylaşmayın
- EmailJS ücretsiz hesabında ayda 200 e-posta limiti vardır
- Spam koruması için form validasyonları mevcuttur

## Sorun Giderme

### Hata: "EmailJS is not defined"
- EmailJS script'inin doğru yüklendiğinden emin olun
- Public Key'in doğru girildiğinden emin olun

### E-posta gelmiyor:
- Spam klasörünü kontrol edin
- Service ID ve Template ID'nin doğru olduğundan emin olun
- EmailJS dashboard'da gönderim loglarını kontrol edin 