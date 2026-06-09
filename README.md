<div align="center">

# SentinelDB360 Lite

**SQL Server tabanlı ERP ve CRM sistemleriniz için sağlık ve yapay zeka hazırlık tarayıcısı**

[Tarayıcıyı indir (Windows)](https://github.com/dmcteknoloji/sentineldb360-lite/releases/latest/download/SentinelDB360.Lite.exe) · [sentineldb360.com/lite](https://sentineldb360.com/lite/) · bir [DMC Bilgi Teknolojileri](https://dmcteknoloji.com) ürünü

</div>

---

## Türkçe

SentinelDB360 Lite, tek bir Windows uygulamasıyla SQL Server veritabanınızı **salt okunur** tarar ve yönetime sunabileceğiniz bir sağlık karnesi ile yapay zeka hazırlık raporu üretir. Teknik kayıt yerine, karar verecek kişinin anlayacağı bir özet alırsınız.

SentinelDB360 ailesinin **giriş ürünüdür**: tam platformu almadan önce sistemlerinizin durumunu görmenizi sağlar.

### Nasıl kullanılır

1. **İndirin** — [SentinelDB360.Lite.exe](https://github.com/dmcteknoloji/sentineldb360-lite/releases/latest/download/SentinelDB360.Lite.exe) (tek dosya, kurulum gerektirmez).
2. **Tarayın** — Uygulamayı çalıştırın, SQL Server bağlantı bilgilerinizi girin. Salt okunur tarama şifreli bir `.bshscan` dosyası üretir.
3. **Yükleyin** — [Yükleme sayfasından](https://sentineldb360.com/lite/) kurumsal e-postanızla doğrulanıp dosyayı yükleyin. Raporunuz e-posta ile gelir ve sayfadan da indirilir.

> Tarama makinesi internete çıkamıyorsa (kapalı ağ / air-gap), oluşan dosyayı internete çıkan başka bir makineden yükleyebilirsiniz.

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

1. **Download** [SentinelDB360.Lite.exe](https://github.com/dmcteknoloji/sentineldb360-lite/releases/latest/download/SentinelDB360.Lite.exe) (single file, no install).
2. **Scan** — run the app, enter your SQL Server connection details. The read-only scan produces an encrypted `.bshscan` file.
3. **Upload** — verify with your corporate email and upload the file at the [upload page](https://sentineldb360.com/lite/). Your report is emailed and downloadable.

All queries are read-only; collected facts are AES-256-GCM encrypted on your device and only the portal can decrypt them. Your business data is never read.

---

<div align="center">

**SentinelDB360 Lite** — bir DMC Bilgi Teknolojileri ürünüdür

[sentineldb360.com](https://sentineldb360.com) · [dmcteknoloji.com](https://dmcteknoloji.com) · iletisim@dmcteknoloji.com

</div>
