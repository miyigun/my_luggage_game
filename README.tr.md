# Öncelikli Geçiş — Bagaj Lojistik Merkezi

Bu repo, klasik “blok kaydırma” mantık oyunlarından ilham alan **tarayıcı tabanlı bir bulmaca oyununu** içerir.  
Amacınız, **sarı “ÖNCELİKLİ” bavulu** ızgara üzerinde doğru şekilde hareket ettirerek **sağ taraftaki kırmızı lazerli çıkış kapısından** çıkarmaktır.

Oyun ağırlıklı olarak **tek bir HTML dosyası** olarak (standalone) çalışır.  
Ek olarak `src/` klasörü altında **React + Vite** ile yazılmış bir sürüm de bulunmaktadır.

---

## Oynanış

- Tahta **6×6** bir ızgaradır.
- Bloklar yalnızca kendi eksenlerinde hareket eder:
  - **Yatay bloklar** sağ/sol
  - **Dikey bloklar** yukarı/aşağı
- Hedef: **ÖNCELİKLİ** (sarı) bloğu sağdaki **çıkışa** ulaştırmak

---

## Özellikler

### 1. Seviyeler
- Toplam **5 adet el yapımı seviye**
- Her seviye bir “terminal/şehir” temasıyla isimlendirilmiştir (İstanbul, Londra, New York…)

### 2. Akıcı Sürükle-Bırak Kontrol
- Mouse ile sürükle-bırak
- Mobil/tablette **dokunmatik** destek
- Hareketler ızgara adımlarına ve çarpışma kurallarına göre kısıtlanır (blokların içinden geçmez)

### 3. Hamle Sayacı & İlerleme
- Seviye başına hamle sayacı
- Kazanınca hamle sayısını gösteren pencere (modal)
- “Sonraki Terminal” ile bir sonraki seviyeye geçiş
- Oyun bitiş ekranında **toplam hamle** ve basit **performans değerlendirmesi**

### 4. Arayüz / Görsel Stil
- Standalone sürümde **Tailwind CSS (CDN)** kullanılır
- **Lucide ikonları**
- “Lojistik kontrol paneli” tarzında arayüz

---

## Proje Yapısı

### Standalone (tek dosya ile çalışır)
- `index.html` — standalone sürüm (HTML + Tailwind CDN + inline `<script>` içinde oyun mantığı)

### React + Vite sürümü (opsiyonel)
- `src/App.jsx` — oyunun React implementasyonu
- `src/main.jsx` — giriş noktası
- `src/index.css` — Tailwind import + temel stiller
- `vite.config.js`, `package.json` — Vite araçları

---

## Başlangıç

### Seçenek A — Standalone çalıştırma (hızlı deneme için önerilir)
1. Repoyu klonlayın:
   ```bash
   git clone https://github.com/miyigun/my_luggage_game.git
   cd my_luggage_game
   ```
2. `index.html` dosyasını tarayıcıda açın.

> İpucu: Bazı tarayıcılar yerel dosya açımında kısıt uygulayabilir. Bu durumda local server kullanın.

Örnek (Python):
```bash
python -m http.server 8000
```
Sonra şurayı açın:
- `http://localhost:8000`

### Seçenek B — React + Vite sürümünü çalıştırma (geliştirme)
1. Bağımlılıkları kurun:
   ```bash
   npm install
   ```
2. Geliştirme sunucusunu başlatın:
   ```bash
   npm run dev
   ```
3. Build:
   ```bash
   npm run build
   ```
4. Build önizleme:
   ```bash
   npm run preview
   ```

---

## 🛠️ Kullanılan Teknolojiler

- HTML / JavaScript
- Tailwind CSS
- Lucide Icons
- (Opsiyonel) React + Vite (`src/` sürümü)

---

## 📌 Notlar

- Kazanma koşulu: “ÖNCELİKLİ” bloğun sağ taraftaki çıkış çizgisine, hedef satıra (row) gelecek şekilde ulaştırılmasıdır.
- Repo’da şu an **iki farklı uygulama** (standalone ve React) bulunuyor. İleride bakım için birini “ana sürüm” olarak seçmek iyi olabilir.

---

## 📜 Lisans

MIT Lisansı (`LICENSE` dosyasına bakınız).