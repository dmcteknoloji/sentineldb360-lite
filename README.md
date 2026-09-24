<div align="center">

# SentinelDB360 Lite

**SQL Server tabanlı ERP ve CRM sistemleriniz için sağlık ve yapay zeka hazırlık tarayıcısı**

[Tarayıcıyı indir · Download (Windows)](https://sentineldb360.com/lite/) · bir [DMC Bilgi Teknolojileri](https://dmcteknoloji.com) ürünü

</div>

---

## Türkçe

SentinelDB360 Lite, tek bir Windows uygulamasıyla SQL Server veritabanınızı **salt okunur** tarar ve yönetime sunabileceğiniz bir sağlık karnesi ile yapay zeka hazırlık raporu üretir. Teknik kayıt yerine, karar verecek kişinin anlayacağı bir özet alırsınız.

SentinelDB360 ailesinin **giriş ürünüdür**: tam platformu almadan önce sistemlerinizin durumunu görmenizi sağlar.

### Nasıl kullanılır

1. **İndirin** — [sentineldb360.com/lite üzerinden](https://sentineldb360.com/lite/) (tek dosya, kurulum gerektirmez).
2. **Tarayın** — Uygulamayı çalıştırın, SQL Server bağlantı bilgilerinizi girin. Salt okunur tarama şifreli bir `.bshscan` dosyası üretir.
3. **Yükleyin** — [Yükleme sayfasından](https://sentineldb360.com/lite/) kurumsal e-postanızla doğrulanıp dosyayı yükleyin. Raporunuz e-posta ile gelir ve sayfadan da indirilir.

> Tarama makinesi internete çıkamıyorsa (kapalı ağ / air-gap), oluşan dosyayı internete çıkan başka bir makineden yükleyebilirsiniz. Adımlar aşağıda.

### Kapalı ağda (air-gap) kullanım

1. Uygulamayı tarama makinesinde çalıştırın, e-posta alanını **boş bırakın**. Bu durumda uygulama internete bağlanmaz, yalnız şifreli paketi üretir.
2. Tarama bitince **Çıktı klasörünü aç** düğmesine basın. Paketin adı `SentinelSec_<sistem>_<tarih>.bshscan` biçimindedir.
3. Dosyayı kurumunuzun onaylı aktarım yöntemiyle (USB, dosya aktarım sunucusu vb.) internete çıkan bir makineye taşıyın.
4. O makinede [sentineldb360.com/lite](https://sentineldb360.com/lite/) yükleme sayfasını açın, kurumsal e-postanızı doğrulayıp dosyayı yükleyin.

Paket cihazda şifrelenir ve yalnız portal açabilir. Aktarım sırasında dosyanın içeriği okunamaz.

### İndirilen dosyayı doğrulama

Uygulama henüz kod imzası taşımıyor; Windows SmartScreen ilk çalıştırmada uyarı gösterebilir. Dosyanın değiştirilmediğini SHA-256 özetiyle doğrulayın:

```powershell
Get-FileHash .\SentinelDB360-Lite.exe -Algorithm SHA256
```

Çıkan değeri indirme sırasında size gösterilen özetle karşılaştırın. GitHub [sürüm sayfasındaki](https://github.com/dmcteknoloji/sentineldb360-lite/releases/latest) `SHA256.txt` dosyası o sürümün özetini içerir. Değerler aynı değilse dosyayı çalıştırmayın ve iletisim@dmcteknoloji.com adresine yazın.

### Güvenlik

- Tüm sorgular **salt okunur** (SELECT / DMV); üretim sistemine yazma yapılmaz.
- Toplanan teknik bulgular cihazınızda **AES-256-GCM** ile şifrelenir; anahtar sunucunun RSA açık anahtarıyla sarmalanır.
- Şifreli dosya yalnızca portalın özel anahtarıyla (KMS) açılabilir. Tarayıcı hiçbir iş zekâsı içermez.
- İş veriniz (tablolardaki kayıtlar) **okunmaz**; yalnızca yapılandırma ve sağlık metrikleri toplanır.

### Gereksinimler

| | |
|---|---|
| İşletim sistemi | Windows 10/11, Windows Server 2016+ |
| Hedef veritabanı | SQL Server 2016+ (on-prem veya Azure SQL MI) |
| Gereken izin | Salt okunur; sunucu durumunu görüntüleme (VIEW SERVER STATE) yeterli |
| Kurulum | Yok (tek dosya, ~50 MB) |

---

## English

SentinelDB360 Lite scans your SQL Server database **read-only** with a single Windows app and produces a board-ready health report plus an AI-readiness assessment. It is the **entry product** of the SentinelDB360 family.

1. **Download** from [sentineldb360.com/lite](https://sentineldb360.com/lite/) (single file, no install).
2. **Scan** — run the app, enter your SQL Server connection details. The read-only scan produces an encrypted `.bshscan` file.
3. **Upload** — verify with your corporate email and upload the file at the [upload page](https://sentineldb360.com/lite/). Your report is emailed and downloadable.

All queries are read-only; collected facts are AES-256-GCM encrypted on your device and only the portal can decrypt them. Your business data is never read.

**Air-gapped networks.** Leave the email field empty: the app then makes no network call and only writes the encrypted package (`SentinelSec_<system>_<date>.bshscan`, reachable via **Open output folder**). Move the file with your approved transfer method to a machine with internet access and upload it at [sentineldb360.com/lite](https://sentineldb360.com/lite/).

**Verifying the download.** The executable is not code-signed yet, so SmartScreen may warn on first run. Check the SHA-256 digest with `Get-FileHash .\SentinelDB360-Lite.exe -Algorithm SHA256` and compare it with the digest shown at download time or with `SHA256.txt` on the [release page](https://github.com/dmcteknoloji/sentineldb360-lite/releases/latest). If they differ, do not run the file.

---

<div align="center">

**SentinelDB360 Lite** — bir DMC Bilgi Teknolojileri ürünüdür

[sentineldb360.com](https://sentineldb360.com) · [dmcteknoloji.com](https://dmcteknoloji.com) · iletisim@dmcteknoloji.com

</div>
