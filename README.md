🛰️ A.F.E.T. | Advanced Framework for Emergency Tracking
Afet Yönetimi ve Operasyonel Komuta Terminali
A.F.E.T., afet sonrası kritik ilk dakikalarda karar vericilere ve operasyonel komuta merkezlerine yüksek doğruluklu, düşük gecikmeli görsel veri sunmak amacıyla geliştirilmiş bir Karar Destek Sistemidir (DSS). Özellikle İstanbul odağında Marmara Bölgesi için optimize edilen bu terminal; lojistik hat analizi, enkaz bölgeleme ve güvenli alan koordinasyonunu tek bir merkezde birleştirir.

📌 Proje Özeti
Sistem, afet anındaki kaos ortamında veri kirliliğini eleyerek operatörün en doğru kararı en kısa sürede vermesini hedefler. Geleneksel ağır GIS yazılımlarının aksine, düşük donanım kaynaklarıyla maksimum performans sağlayan bir yapıya sahiptir.

Odak Noktası: Lojistik hat analizi, dinamik zonlama ve eş zamanlı operasyonel izleme.

Hedef Kullanıcı: Afet Koordinasyon Merkezleri (AKOM, AFAD vb.) ve saha komuta birimleri.

🛠 Teknik Mimari ve Teknolojiler
Proje, kriz anlarında kesintisiz hizmet verebilmek adına Thin-Client (İnce İstemci) mimarisi üzerine inşa edilmiştir.

Harita Motoru: Leaflet.js (Hafif, modüler ve yüksek genişletilebilirlik).

Coğrafi Veri Katmanı: ArcGIS World Imagery (Gerçek zamanlı ve yüksek çözünürlüklü uydu entegrasyonu).

Veri Görselleştirme: Dinamik poligon ve polyline algoritmaları ile desteklenen Zoning (Bölgeleme) ve rota planlama motoru.

UI/UX Standartları:

Dark-Ops Interface: Göz yorgunluğunu minimize eden ve enerji tasarrufu sağlayan, düşük fotonlu renk paleti.

Tipografi: Operasyonel okunabilirliği en üst düzeye çıkaran Orbitron ve Rajdhani font sistemleri.

🛡 Temel Fonksiyonel Özellikler

1. Senkronize Çift Panel Sistemi (Dual-Pane Sync)
   Operasyonel farkındalığı artırmak amacıyla sistem iki ana katmana ayrılmıştır:

Sol Panel: Bölgesel Hasar Analizi ve Enkaz Durumu.

Sağ Panel: Operasyonel Rota ve Lojistik Planlama.

Özellik: Panellerden birinde yapılan Pan/Zoom hareketi, diğer panele aktarılır. Bu, hasar ve müdahale hattı arasındaki iletişimi hızlandırır.

2. Akıllı Lojistik Katmanları
   Güzergahlar, aracın tipine ve görev önceliğine göre dinamik olarak sınıflandırılır:

🔵 Ana İkmal Hatları (Blue Route): Ağır vasıta ve yardım tırları için yüksek kapasiteli yollar.

🟢 Acil Müdahale Hatları (Green Route): Sadece ambulans ve hafif arama-kurtarma ekiplerine özel, optimize edilmiş geçiş rotaları.


3. Kritik Bölge Analizi (Dynamic Zoning)
🔴 Kırmızı Bölge (Critical Zone): Enkaz yoğunluğu, yangın veya gaz sızıntısı gibi ikincil risklerin bulunduğu yüksek riskli poligonlar.

🟢 Yeşil Bölge (Safe Zone): Coğrafi olarak güvenli, altyapısı korunmuş ve toplu barınmaya uygun alanlar.

🚀 Kurulum ve Çalıştırma
Bash

# Depoyu klonlayın

git clone https://github.com/kullaniciadi/afet-terminal.git

# Proje dizinine gidin

cd afet-terminal

# Bağımlılıkları yükleyin (Örnek npm kullanımı)

npm install

# Uygulamayı başlatın

npm start OR python -m http.server

📅 Yol Haritası (Roadmap)
[ ] Gerçek zamanlı IoT sensör verilerinin haritaya entegrasyonu.

[ ] İHA (UAV) görüntülerinin anlık olarak katman olarak eklenmesi.

[ ] Çevrimdışı (Offline) çalışma modu için vektör tile desteği.
