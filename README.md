# Emre Güzel — Kişisel Portfolio

Bilgisayar mühendisi adayı için tasarlanmış, tek sayfalık kişisel portfolio web sitesi. Masaüstünde "rail" biçiminde bir yan navigasyon ve sayfa geçişleriyle çalışan, bağımlılıksız (zero-dependency) statik bir sitedir.

**Canlı:** GitHub Pages üzerinden yayınlanmaktadır — `github.com/EmreGuezel/Portfolio`

---

## Genel Bakış

Site, tek bir `index.html` dosyası içinde barındırılan kendi kendine yeten bir uygulamadır. Harici bir CSS/JS dosyası, paket yöneticisi veya derleme adımı yoktur; tarayıcıda doğrudan açılabilir.

**Bölümler:**

| Sayfa | İçerik |
| --- | --- |
| **Ana Sayfa** | Tanıtım ve kısa özet |
| **Hakkımda** | Profil özeti, eğitim, diller |
| **Deneyim** | İş deneyimi ve stajlar |
| **Projeler & Yetenekler** | Proje kartları ve teknik yetkinlikler |
| **İletişim** | İletişim kanalları ve CV indirme |

**Öne çıkan özellikler:**

- Çift dilli arayüz (Türkçe / İngilizce) — çalışma zamanında metin değişimi
- Sabit yan navigasyon ve yumuşak kaydırmalı sayfa geçişleri
- Tamamen responsive (mobil uyumlu) yerleşim
- Fraunces / Inter / IBM Plex Mono tipografi sistemi
- CSS değişkenleri üzerine kurulu tema (renk, tipografi, boşluk)

---

## Teknoloji

**Bağımlılık yok** — framework, build aracı veya npm paketi kullanılmamaktadır.

- **HTML5** — semantik yapı
- **CSS3** — özel özellikler (custom properties), Flexbox, Grid, media query'ler
- **Vanilla JavaScript** — sayfa yönlendirme, dil değişimi, etkileşimler
- **Google Fonts** — Fraunces, Inter, IBM Plex Mono

---

## Proje Yapısı

```
portfolio/
├── index.html            # Sitenin tamamı (yapı + stil + script)
├── Emre_Guzel_cv.pdf     # İndirilebilir CV
├── resim.jpg             # Profil fotoğrafı
└── README.md
```

---

## Çalıştırma

Derleme adımı gerekmez. İki seçenek:

**1. Doğrudan açma**

`index.html` dosyasına çift tıklayın veya tarayıcıya sürükleyin.

**2. Yerel sunucu (önerilir)**

Bazı tarayıcılar `file://` protokolünde font ve göreli yolları kısıtlayabilir:

```bash
python -m http.server 8000
```

Ardından `http://localhost:8000` adresini açın.

---

## Yayınlama

Site statik olduğu için herhangi bir statik barındırma hizmetiyle çalışır.

**GitHub Pages:**

1. Depoyu `main` dalına gönderin
2. **Settings → Pages** bölümüne gidin
3. Source olarak `main` dalını ve `/ (root)` klasörünü seçin
4. Site `https://emreguezel.github.io/Portfolio/` adresinde yayınlanır

**Vercel / Netlify:** Depoyu bağlayın, build komutu boş bırakılır, yayın dizini kök (`/`) olarak ayarlanır.

---

## Geliştirme Notları

**Tema değişkenleri** — `index.html` içindeki `:root` bloğundan renk ve tipografi tek noktadan değiştirilebilir:

```css
:root {
  --paper: #F7F7F4;    /* arka plan */
  --ink: #1C1D1F;      /* ana metin */
  --accent: #2B5D5A;   /* vurgu rengi */
}
```

**Dil içeriği** — çeviriler `index.html` sonundaki `translations` nesnesinde tanımlıdır. Yeni bir metin eklemek için hem HTML'e `data-i18n` anahtarı eklenir hem de `translations` nesnesine `tr` ve `en` karşılıkları yazılır.

**Not:** CV bağlantısı büyük/küçük harfe duyarlıdır. Dosya adı değiştirilirse `index.html` içindeki referansın da güncellenmesi gerekir (Linux tabanlı sunucularda sorun çıkarır).

---

## İletişim

**Emre Güzel** — Bilgisayar Mühendisi

- E-posta: [emreguzel2002@gmail.com](mailto:emreguzel2002@gmail.com)
- LinkedIn: [linkedin.com/in/emre-guezel](https://www.linkedin.com/in/emre-guezel/)
- GitHub: [github.com/EmreGuezel](https://github.com/EmreGuezel)
- Konum: Ankara, Türkiye
