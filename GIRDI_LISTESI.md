# Girdi Kontrol Listesi

Petkim forecast zincirine giren dosyaların listesi. Tanıtım sırasında hiçbir input atlanmasın diye tutulur. Başlangıç listesi devir paketindeki input kataloğundan alındı (24.11.2026); liste henüz ana modelin dış bağlantılarıyla doğrulanmadı. Dosyanın ne olduğu ve nasıl kullanıldığı burada değil, `inputs/` altındaki tanım dosyasında yazar; bu liste yalnız ad, katman ve durum tutar.

**Durum:** ✅ tanım dosyası var ve dosyayla doğrulandı · 🔍 dosya geldi, analiz edildi, tanım bekliyor · ⏳ dosya bekleniyor · ❔ kapsam kararı bekleniyor

| # | Input (devirdeki adıyla) | Katman | Durum | Tanım dosyası |
|---|---|---|---|---|
| 1 | Forecast / Cost Model RAW DATA | RAW | 🔍 | – |
| 2 | Forecast Planned (`Satış ve Ticari Bütçe`) | Planned | 🔍 | – |
| 3 | Hammadde Planı RAW DATA | RAW | 🔍 | – |
| 4 | Hammadde Planı Planned | Planned | 🔍 | – |
| 5 | Model Alt Çalışması | Konsolidasyon | 🔍 | – |
| 6a | Üretim Planı RAW DATA | RAW | 🔍 | – |
| 6b | Üretim Planı Planned | Planned | 🔍 | – |
| 7 | PETKİM&STAR Gas Power Prices | Input | 🔍 | – |
| 8 | Ana model (`Budget_Model_Planned.xlsb`) | Model | 🔍 (yalnız dönem ve stok bağlantısı okundu) | – |
| 9 | Financial Results Planned | Çıktı | 🔍 (yalnız sayfa ve bağlantı listesi okundu) | – |
| 10 | IFRS Hammadde / Mamul / Yarımamul stok envanter raporları | Stok | ⏳ (nasıl ele alınacağı açık: `ACIK_SORULAR.md` #10) | – |
| 11 | STAR Financial Model (Hammadde Planned'a STAR verisi) | Harici model | ⏳ | – |
| 12 | Rapor 42 maliyet raporları, SATIŞLAR | Raporlama | ⏳ | – |
| 13 | Results düzeltme dosyaları (Upside Downside Effects, Personnel CC Chargeback, STAR Results) | Results | ⏳ (Upside/Downside ayrıca tanıtılacak) | – |
| 14 | 2026 Budget Model 65 USD Brent | Bütçe | ⏳ | – |

**24.11.2026:** Kasım 2026 Planned (v2) klasöründen on dosya geldi ve okundu (#1–#9). Tanım dosyaları "önce göster, sonra yaz" kuralıyla sırayla yazılacak. Dosyaların birbirine bağlandığı klasörler karışık görünüyor (ilk versiyon, v2 ve 0+30 klasörleri); çıktı için belirleyici olan son versiyondur (`KARAR_GUNLUGU` "Tur 1 panel cevapları").

**Not:** "Katman" sütunu devirdeki gözlemdir; her input tanıtılırken teyit edilir. Ana model ve Financial Results'ın input mu çıktı mı sayılacağı henüz karara bağlanmadı.
