# Threat Intel Lookup

Palo Alto URL Filtering, VirusTotal, AbuseIPDB, Shodan ve Talos Intelligence ile IP ve domain sorgulaması yapabileceğiniz, tek dosyalı browser tabanlı araç.

## Özellikler

- 📂 **Dosya import** — txt, csv, log dosyaları (drag & drop destekli)
- 🧹 **Defang çözümü** — `212[.]11[.]64[.]105` → `212.11.64.105` otomatik
- 🔗 **5 kaynak için hızlı linkler** — PA / VT / AbuseIPDB / Shodan / Talos
- 🔑 **VirusTotal API** — Otomatik tarama + skor gösterimi
- 📊 **Durum yönetimi** — Zararlı / Şüpheli / Temiz / Bilinmiyor
- 📥 **CSV export** — Tüm sonuçları tek tıkla indir
- 📋 **IOC kopyala** — Zararlı/şüpheli listeyi panoya kopyala
- 🔍 **Filtre & sırala** — Durum ve türe göre filtrele

## Kullanım

### Yöntem 1 — GitHub Pages (Önerilen)

1. Bu repoyu fork'layın
2. `Settings → Pages → Deploy from branch → main` seçin
3. `https://kullaniciadiniz.github.io/threat-lookup` adresinden erişin

### Yöntem 2 — Yerel Kullanım

`index.html` dosyasını tarayıcıda açın. Backend gerekmez.

## VirusTotal API

1. [virustotal.com/gui/join-us](https://www.virustotal.com/gui/join-us) adresinden ücretsiz hesap açın
2. API anahtarınızı kopyalayın
3. Uygulamada API alanına yapıştırıp **Kaydet**'e tıklayın
4. **VT Tara** düğmesiyle otomatik taramayı başlatın

> Ücretsiz plan: 4 istek/dakika — büyük listeler için biraz zaman alır

## Desteklenen Formatlar

```
212[.]11[.]64[.]105          # Defanged IP
helper[.]leuleu[.]net        # Defanged domain
45.76.155.202                # Normal IP
fortinet-vpn.com             # Normal domain
hxxps://checkpoint-vpn[.]com # URL (domain çıkarılır)
```

## Kontrol Edilen Kaynaklar

| Kısaltma | Servis | URL |
|---|---|---|
| PA | Palo Alto URL Filtering | urlfiltering.paloaltonetworks.com |
| VT | VirusTotal | virustotal.com |
| AB | AbuseIPDB | abuseipdb.com |
| SH | Shodan | shodan.io |
| TL | Talos Intelligence | talosintelligence.com |

## Notlar

- Tamamen client-side — hiçbir veri sunucuya gönderilmez
- VirusTotal API anahtarı yalnızca tarayıcının localStorage'ında saklanır
- Palo Alto sitesi CAPTCHA gösterebilir; PA linkleri manuel kontrol içindir
