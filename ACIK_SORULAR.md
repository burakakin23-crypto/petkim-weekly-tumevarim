# Açık Sorular

Cevabı henüz verilmemiş konular. Soru numaraları sabittir (#1 dönem, #2 birimler, #3 ürün listesi 24.11.2026'da cevaplandı ve çıktı). Soruların dosyadaki gözlemle birlikte tam metni soru panelindedir: https://claude.ai/artifact/Gn4D82qQUQnFFTSTF8YtwU. Cevaplanan soru buradan çıkar; sonucu `KARAR_GUNLUGU.md`'ye (karar) ya da ilgili `inputs/<dosya_adı>.md`'ye (input bilgisi) yazılır.

**Etiketler:** `[Kullanıcı]` = kullanıcıyla cevaplanacak · `[Petkim ekibine sorulacak]` = Petkim ekibiyle birlikte cevaplanacak.

| # | Soru | Etiket | İlgili input | Açılış tarihi |
|---|---|---|---|---|
| 4 | G1-21 ürünü hangi gruba ait? (Planned'da YYPE grubunda toplanıyor, fiyatı AYPE seviyesinde.) | [Petkim ekibine sorulacak] (ticaret) | Forecast Planned | 24.11.2026 |
| 5 | I457 UV ve S 00356 YY, YYPE grubuna dahil mi? | [Petkim ekibine sorulacak] (ticaret) | Forecast Planned | 24.11.2026 |
| 6 | Bütenin birimi gerçekten KG mı, yoksa ton mu? | [Petkim ekibine sorulacak] (planlama) | Hammadde Planı | 24.11.2026 |
| 7 | Toluen ihracat miktarına Reformat ihracatı eklenir kuralı geçerli mi? | [Petkim ekibine sorulacak] | Model Alt Çalışması | 24.11.2026 |
| 8 | Bir ay içindeki forecast periyotlarının adları ve sırası ne (0+30/31, Planned, sonrası)? | [Petkim ekibine sorulacak] | Genel | 24.11.2026 |
| 9 | STAR nafta fiyatı nasıl belirleniyor? ("İthal + sabit prim" kuralı geçerli değil dendi.) | [Petkim ekibine sorulacak] | Hammadde Planı | 24.11.2026 |
| 10 | Stok girdisi otomasyonda nasıl ele alınacak (haftalıkta mı güncellenir, aylık çalışmadan mı gelir)? | [Petkim ekibine sorulacak] | Stok raporları | 24.11.2026 |
| 11 | Model Alt'a hiç bağlı olmayan ürünlerden (Planned'da olup Model Alt'a gitmeyenler; RAW'da olup Planned'da olmayanlar) hacim gelirse hangi stok ve maliyet yapısına bağlanacak? | [Petkim ekibine sorulacak] (ticaret) | Forecast RAW / Planned, Model Alt | 24.11.2026 |
| 12 | Ticari ürünlerde yanlış olan blok adları mı, bağlantılar mı? (Bir blok başka ürünün satırını okuyor; iki ürün birden fazla blokta geçiyor.) | [Petkim ekibine sorulacak] | Model Alt Çalışması | 24.11.2026 |
| 13 | Üretim Planı Planned'da AYPE satırlarındaki kayma (RAW'daki G 1/21 satırı Planned'da yok; AYPE-2 duruş günü kayan satırdan okunuyor) hata mı? | [Petkim ekibine sorulacak] (planlama) | Üretim Planı Planned | 24.11.2026 |
| 14 | Üretim Planı Planned'da elle yazılan ağır nafta günlük tüketimi nereden geliyor? | [Petkim ekibine sorulacak] (planlama) | Üretim Planı Planned | 24.11.2026 |
| 15 | Üretim Planı RAW DATA'yı kim hazırlıyor, ne sıklıkla geliyor? | [Petkim ekibine sorulacak] | Üretim Planı RAW | 24.11.2026 |
| 16 | Hammadde fiyatlarının (VCM, etilen, amonyak, PGP, CGP) kaynağı Forecast RAW dosyasının "Hammadde" sayfası mı? | [Petkim ekibine sorulacak] | Hammadde Planı Planned | 24.11.2026 |
| 17 | Gas Power Prices dosyasını kim hazırlıyor, kaynağı ne? (Bütün değerler elle yazılmış.) | [Petkim ekibine sorulacak] | Gas Power Prices | 24.11.2026 |
| 18 | Doğalgaz ve elektrik miktarı haftalıkta güncellenmiyor mu? (Model Alt miktarı bütçe modelinden, yalnız fiyatı Gas Power'dan okuyor.) | [Petkim ekibine sorulacak] | Gas Power Prices, Model Alt | 24.11.2026 |
| 19 | Kasım 2026 Planned'da Ekim kapanış stoğu yetişmiş miydi? (Dosyalara göre forecast Kasım'dan başlıyor.) | [Petkim ekibine sorulacak] | Ana model | 24.11.2026 |
| 20 | Dosyalardaki İngilizce grup adları Türkçe adlarla nasıl eşleşiyor (LDPE = AYPE, LDPE-T = AYPE-T, HDPE = YYPE)? | [Petkim ekibine sorulacak] | Genel | 24.11.2026 |
| 21 | Modelde bariz hata görüldüğünde ne yapılacak: yalnız bildirmek mi, kendi hesabında doğru mantığı kullanıp farkı ayrı göstermek mi? (Panel cevabı ile toplantı notu örtüşmüyor.) | [Kullanıcı] | Genel | 24.11.2026 |
| 22 | Güncel girdi gelmediğinde önceki versiyonla devam etme kuralı (hangi versiyonun kullanıldığını yazarak) bütün girdiler için geçerli mi? | [Kullanıcı] | Genel | 24.11.2026 |
| 23 | Girdi tanım şablonuna dönem ve versiyon alanları eklensin mi? | [Kullanıcı] | Genel | 24.11.2026 |
| 24 | STAR payı %12 hangi tutara uygulanıyor ("netting üzerinden")? | [Kullanıcı] | Financial Results | 24.11.2026 |
| 25 | Toplantı notundaki iki yaklaşımdan hangisi bu repo, hangisi `petkim-weekly`? | [Kullanıcı] | Genel | 24.11.2026 |
| 26 | Repoya kişi adı yazılsın mı, yalnız ekip adı mı? | [Kullanıcı] | Genel | 24.11.2026 |
| 27 | `Petkim Waterfall Forecast Vs Budget` dosyası sunumun doğrudan kaynağı; girdi listesinde yok. Kim hazırlıyor, Financial Results'tan mı besleniyor, bütçe kolonunun kaynağı ne? | [Petkim ekibine sorulacak] | Waterfall dosyası, Sunum | 26.11.2026 |
| 28 | Sunum besleme dosyasında Ethylene satırının LF hacmi ve fiyatı formülde `*0` ile sıfırlanmış. Bilinçli bir müdahale mi, gerekçesi ne? | [Petkim ekibine sorulacak] | Sunum besleme dosyası | 26.11.2026 |
| 29 | Yıl sonu STAR katkısı (S02) aylık 9+3 Financial Results ile Planned v2 Financial Results'ın karışımından hesaplanıyor. Kural bu mu, haftalıkta hangi dosyalar esas? | [Petkim ekibine sorulacak] | Financial Results, Sunum | 26.11.2026 |
| 30 | Sunumdaki stok slaytları (Ticari ürün stok seviyesi ve satış karşılama; Petkim üretilen ürün stokları, önceki ay kapanışı) bu kolun çıktısına dahil mi? | [Kullanıcı] | Stok raporları, Sunum | 26.11.2026 |
| 31 | S10'daki ticari ürün listesi Waterfall dosyasının sabit satırlarından geliyor (kaynakta bir satır atlanmış; "Etylene" yazımı). Liste Forecast RAW'ın ticari bölümüyle mi eşleşmeli? | [Petkim ekibine sorulacak] (ticaret) | Waterfall dosyası, Forecast RAW | 26.11.2026 |
| 32 | Yıl sonu değerleri aylık (monthly) forecast'tan beslenecek: hangi aylık dosyadan (ör. 9+3 Financial Results) ve nasıl — yıl sonu doğrudan aylık dosyadan mı alınır, yoksa haftalıkta üretilen ay değeri aylık dosyanın yıl sonuna yerine konarak mı? (Ay değeri haftalıktan üretilir.) | [Kullanıcı] | Sunum, aylık forecast | 26.11.2026 |
