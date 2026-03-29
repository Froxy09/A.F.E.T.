#AFET
Gemini şunu dedi:
GitHub üzerindeki A.F.E.T. (Afet Yönetimi ve Operasyonel Komuta Terminali) projen için profesyonel, siber güvenlik ve gömülü sistemler estetiğine (Cyberpunk/Military-grade) uygun bir README.md taslağı hazırladım.

Bu taslak, paylaştığın HTML kodlarındaki görsel dilden ve teknik detaylardan (Leaflet.js, ArcGIS, siber veri akışı) ilham almıştır.

🚀 A.F.E.T. :: Afet Yönetimi ve Operasyonel Komuta Terminali
A.F.E.T. (Marmara Bölge Komuta Terminali), afet sonrası koordinasyon, lojistik rota takibi ve hasar analizi için tasarlanmış yüksek vizyonlu bir terminal arayüzüdür. Proje, özellikle Marmara Bölgesi (İstanbul merkezli) operasyonel süreçlerini dijitalleştirmeyi ve komuta merkezlerine anlık görsel veri sunmayı amaçlar.

🛠 Öne Çıkan Özellikler
Çift Panelli Analiz Terminali: Bölgesel hasar analizi (Sol) ve Operasyonel rota takibi (Sağ) ekranlarının eş zamanlı (sekronize) çalışması.

Dinamik Rota Takibi:

🔵 Lacivert Hatlar: Ana ikmal ve lojistik yolları.

🟢 Yeşil Hatlar: Acil müdahale ve tahliye rotaları.

Risk Bölgeleme (Zonlama):

🔴 Kritik Enkaz Alanları: Yüksek riskli yıkım bölgelerinin poligonlarla işaretlenmesi.

🌳 Güvenli Toplanma Alanları: Tahliye sonrası güvenli noktaların belirlenmesi.

Karanlık Mod & Cyber-UI: 'Orbitron' ve 'Rajdhani' fontları ile güçlendirilmiş, düşük ışıklı komuta merkezleri için optimize edilmiş yüksek kontrastlı arayüz.

ArcGIS Uydu Entegrasyonu: Gerçek zamanlı dünya uydu görüntüleri üzerinde özel katman (Dark Masking) uygulaması.

📸 Ekran Görüntüsü Tasarımı
Terminal arayüzü, afet anında karar vericilerin dikkatini dağıtmayacak, sadece operasyonel veriye odaklanan bir yapıya sahiptir:

Header: Gerçek zamanlı UTC saat akışı ve sistem durum göstergesi.

Map: Leaflet.js tabanlı, sınırlandırılmış (Marmara odaklı) interaktif harita katmanları.

🚀 Kurulum ve Kullanım
Proje, herhangi bir sunucu gereksinimi duymadan (Client-side) çalışmaktadır.

Depoyu klonlayın:

Bash
git clone https://github.com/Froxy09/A.F.E.T..git
Proje klasörüne gidin.

index.html dosyasını modern bir tarayıcıda açın.

🧬 Teknik Altyapı
Harita Motoru: Leaflet.js

Harita Katmanı: ArcGIS World Imagery

Tipografi: Google Fonts (Orbitron, Rajdhani, Share Tech Mono)

Veri Yapısı: Operasyonel rotalar ve poligonlar JSON tabanlı koordinat dizileri (L.polyline, L.polygon) ile yönetilmektedir.

🗺 Yol Haritası (Roadmap)
[ ] Gerçek zamanlı deprem API entegrasyonu (AFAD/Kandilli).

[ ] Gömülü sistemler (ESP32/Raspberry Pi) üzerinden gelen saha verilerinin (sıcaklık, nem, gaz) haritaya işlenmesi.

[ ] Saha ekipleri için mobil uyumlu GPS takip arayüzü.

[ ] WebSocket ile merkezi komuta odasından tüm terminallere anlık bildirim gönderimi.
