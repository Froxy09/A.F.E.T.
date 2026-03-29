# 🛰️ A.F.E.T.

### Analitik Fotogrametri ve Etki Takibi

🛰️ A.F.E.T. | Analitik Fotogrametri ve Etki Takibi afet sonrası kritik ilk dakikalarda karar vericilere ve operasyonel komuta merkezlerine yüksek doğruluklu, düşük gecikmeli görsel veri sunmak amacıyla geliştirilmiş bir Karar Destek Sistemidir (DSS). Özellikle İstanbul odağında Marmara Bölgesi için optimize edilen bu terminal; lojistik hat analizi, enkaz bölgeleme ve güvenli alan koordinasyonunu tek bir merkezde birleştirir.

📌 Proje Özeti
Seyrü Feza (AFET), deprem sonrasında kurtarma ekiplerinin sahada yaşadığı "bilgi körlüğü" problemini uzay teknolojileriyle çözen otonom bir karar destek platformudur. Sistemimiz; rasathanelerden gelen anlık sismik veriler ile yerli uydumuz İMECE ve Sentinel-1'den alınan görüntüleri yapay zekâ ile harmanlayarak enkaz altındaki yolları saniyeler içinde saptar. Bu hibrit veri füzyonu sayesinde, ekipleri tehlikelerden uzak tutarak doğrudan hedefe ulaştıran en güvenli "Altın Rota" dinamik olarak çizilir.
## 🛠 Teknik Mimari ve Teknolojiler

Proje, kriz anlarında kesintisiz hizmet verebilmek adına *Thin-Client (İnce İstemci)* mimarisi üzerine inşa edilmiştir.

| Bileşen            | Teknoloji              | Fonksiyon                                                                |
| :----------------- | :--------------------- | :----------------------------------------------------------------------- |
| *Harita Motoru*  | Leaflet.js ve windy.com  | Hafif, modüler ve yüksek genişletilebilirlik.                            |
| *Coğrafi Veri*   | ArcGIS World Imagery | Gerçek zamanlı ve yüksek çözünürlüklü uydu entegrasyonu.                 |
| *Görselleştirme* | Custom Zoning Engine | Dinamik poligon ve polyline algoritmaları ile desteklenen rota planlama. |
| *Arayüz (UI)*    | Dark-Ops Interface   | Göz yorgunluğunu minimize eden düşük fotonlu renk paleti.                |
| *Tipografi*      | Orbitron & Rajdhani  | Operasyonel okunabilirliği en üst düzeye çıkaran font sistemleri.        |
| *Uydu Verileri*  | İMECE(TÜRKİYE)       |                                                                          |

---

## 🛡 Temel Fonksiyonel Özellikler

### 1. Senkronize Çift Panel Sistemi (Dual-Pane Sync)

Operasyonel farkındalığı artırmak amacıyla sistem iki ana katmana ayrılmıştır:

- *Sol Panel:* Bölgesel Hasar Analizi ve Enkaz Durumu.
- *Sağ Panel:* Operasyonel Rota ve Lojistik Planlama.
- *Özellik:* Panellerden birinde yapılan Pan/Zoom hareketi, diğer panele otomatik aktarılır. Bu, hasar ve müdahale hattı arasındaki iletişimi hızlandırır.

### 2. Akıllı Lojistik Katmanları

Güzergahlar, aracın tipine ve görev önceliğine göre dinamik olarak sınıflandırılır:

- 🔵 *Ana İkmal Hatları (Blue Route):* Ağır vasıta ve yardım tırları için yüksek kapasiteli yollar.
- 🟢 *Acil Müdahale Hatları (Green Route):* Sadece ambulans ve hafif arama-kurtarma ekiplerine özel, optimize edilmiş geçiş rotaları.

### 3. Kritik Bölge Analizi (Dynamic Zoning)

- 🔴 *Kırmızı Bölge (Critical Zone):* Enkaz yoğunluğu, yangın veya gaz sızıntısı gibi ikincil risklerin bulunduğu yüksek riskli poligonlar.
- 🟢 *Yeşil Bölge (Safe Zone):* Coğrafi olarak güvenli, altyapısı korunmuş ve toplu barınmaya uygun alanlar.

---
!["Ana Menü"](/Ekran görüntüsü 2026-03-29 125323.png)






---

## Kurulum ve Çalıştırma

bash
# 1. Depoyu klonlayın
git clone https://github.com/Froxy09/AFET

# 2. Proje dizinine gidin
cd afet-terminal

# 3. Bağımlılıkları yükleyin
npm install

# 4. Uygulamayı başlatın
npm start
# VEYA basit bir python sunucusu ile:
python -m http.server 8080
