# keylogger (Windows Forms)

Windows'ta global klavye hook'u ile tuş vuruşlarını kaydedip e‑posta ile gönderen örnek uygulama. Yalnızca eğitim amaçlıdır.

## Özellikler
- Low-level keyboard hook (LL)
- Türkçe karakter desteği
- ~50 tuşta otomatik e‑posta gönderimi
- Başlangıçta çalıştırma (Registry Run)

## Kurulum
1) `keylogger.sln`'i Visual Studio ile açın (.NET Framework 4.7.2)
2) Derleyip çalıştırın (F5)

## SMTP Yapılandırması (Ortam Değişkenleri)
Uygulama e‑posta bilgilerini koddan değil ortam değişkenlerinden okur:
- `SMTP_USERNAME`  Gönderen e‑posta adresi
- `SMTP_PASSWORD`  Uygulama/SMTP şifresi
- (opsiyonel) `SMTP_HOST` varsayılan `smtp.gmail.com`
- (opsiyonel) `SMTP_PORT` varsayılan `587`

PowerShell örnek:
```powershell
$env:SMTP_USERNAME = "example@gmail.com"
$env:SMTP_PASSWORD = "app-password"
$env:SMTP_HOST     = "smtp.gmail.com"
$env:SMTP_PORT     = "587"
```

## Notlar
- Test için formdaki "Test Email Gönder" butonunu kullanabilirsiniz
- Gizli bilgiler depoya eklenmez; sadece ortam değişkenlerinden sağlanır
- Kullanımda yerel yasa ve kurallara uyulmalıdır
