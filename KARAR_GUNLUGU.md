# Karar Günlüğü

Alınan kararlar, tarih ve kısa gerekçeyle. Eski karar silinmez; değiştiğinde altına "yerine geçer: <tarih> <yeni karar>" yazılır.

## Kurulum (24.11.2026)

- **Repo ve iskelet:** `petkim-weekly-tumevarim` Petkim haftalık forecast'ının tümevarım koludur. Repo boştu; `CLAUDE.md`, `KARAR_GUNLUGU.md`, `ACIK_SORULAR.md` ve `inputs/` oluşturuldu. *Gerekçe:* kullanıcının oturum talimatı.
- **Çalışma şekli:** Soru-cevap; her seferinde en fazla 3–4 soru, mümkünse seçenekli; cevap alınmadan varsayımla devam edilmez. *Gerekçe:* kullanıcı talimatı.
- **Belirsiz konular:** "Petkim ekibine sorulacak" diye işaretlenir, `ACIK_SORULAR.md`'ye eklenir, ekiple birlikte cevaplanır. *Gerekçe:* kullanıcı talimatı.
- **Kayıt yerleri:** Kararlar bu dosyada; kalıcı kurallar (klasör yapısı, isimlendirme, birimler, dönem tanımları, input tanıtım şablonu) `CLAUDE.md`'de; input tanımları `inputs/<dosya_adı>.md`'de. *Gerekçe:* kullanıcı talimatı.
- **Input dosyası şablonu:** kaynak, sahibi, güncellenme sıklığı, sayfa/kolon yapısı, birimler, forecast'teki kullanımı, açık sorular. *Gerekçe:* kullanıcı talimatı.
- **Oturum sonu:** Değişiklikler commit + push; kullanıcıya iki üç cümlelik özet. *Gerekçe:* kullanıcı talimatı.
- **Şirket verisi repoya girmez:** `.gitignore` Excel/CSV/zip dosyalarını dışlar (STAR tümevarım reposundaki ile aynı, `.xlsb` eklendi). *Gerekçe:* STAR reposunun kuralı; Petkim modeli `.xlsb`.
  - *Not:* Bu madde kullanıcıya teyide sunuldu; cevap gelene kadar geçici.
  - yerine geçer: 24.11.2026 – kullanıcı "rakam yazılmaz" kuralını STAR'dan aldı; madde kesinleşti (bkz. "STAR yapısından alınanlar").

## Devir paketi (24.11.2026)

- Petkim devir paketi (20.11.2026, eski hesaptaki 11.11 çalışması) STAR'daki gibi kullanılır: ham hali repoya girmez. Eski kararlar (K-01…K-20) kullanıcıya tek tek teyit ettirilip bu günlüğe yazılır; eski bulgular ve açık sorular (S-01…S-19) ilgili input tanıtılırken açık soru olur. Eski `ortak-forecast-metodolojisi` skill'i ve CONFIRMED/LIKELY/UNKNOWN/ASSUMPTION etiketleri alınmaz. *Gerekçe:* kullanıcı kararı; STAR tümevarım kolunda aynı yol izlendi.

## Dönem ve ufuk (24.11.2026)

- Forecast dönemi ve ufku (yalnız çalışılan ay mı, yıl sonuna kadar mı) Petkim ekibine sorulacak; cevap gelene kadar `CLAUDE.md` "Dönem tanımları" boş kalır. *Gerekçe:* kullanıcı kararı; devirde de açık soruydu.

## Birimler (24.11.2026)

- `CLAUDE.md`'deki "Birimler" bölümü ölçü birimlerini (miktar, fiyat, tutar, para birimi) kapsar; üretim üniteleri bu başlıkta değildir. *Gerekçe:* kullanıcı cevabı.

## STAR yapısından alınanlar (24.11.2026)

STAR tümevarım reposundan (`star-weekly-tumevarim`) şunlar alındı; içerikleri Petkim'e göre yeniden yazılır, STAR'a özgü kural taşınmaz. *Gerekçe:* kullanıcı kararı.
- **Girdi kontrol listesi:** `GIRDI_LISTESI.md` (hangi input var, durumu).
- **Eşzamanlı çalışma:** tek dal `main`; her yazmadan önce `git pull --rebase`; küçük commit, hemen push; çakışmada satırlar birleştirilir, anlamca çelişki kullanıcıya sorulur.
- **Rakam yazılmaz:** input dosyalarına gerçek rakam ya da şirket verisi yazılmaz; yalnız yapı ve anlam.
- **`skills/` klasörü:** iş sırası ve bakış açısı skill'leri. Hangi skill'lerin açılacağı ayrıca sorulacak.

## Birimler, ürünler, girdi listesi, isimlendirme (24.11.2026)

- **Ölçü birimleri** Petkim ekibine sorulacak (`ACIK_SORULAR.md` #2); o zamana kadar her input'ta ayrıca teyit edilir. *Gerekçe:* kullanıcı kararı.
- **Ürün ve ürün grubu listesi** Petkim ekibine sorulacak (`ACIK_SORULAR.md` #3). *Gerekçe:* kullanıcı kararı; devirdeki gruplar onaysızdı.
- **Dönem/ufuk** açık sorusu `ACIK_SORULAR.md` #1 olarak kaydedildi.
- **Girdi listesi** devirdeki 14 input ile başlatıldı, hepsi "⏳ dosya bekleniyor". *Gerekçe:* kullanıcı kararı.
- **İsimlendirme:** `inputs/` tanım dosyası dönemsiz sabit ad taşır; gerçek ad kalıbı dosyanın içinde yazılır. *Gerekçe:* kullanıcı kararı; her hafta aynı tanım güncellenir, sürüm başına kopya oluşmaz.

## Amaç ve yön (24.11.2026)

- **Nihai hedef (STAR gibi):** Yalnız girdiler verilir, ana modelin çıktısı üretilir. Ana model ve Financial Results yalnız öğrenmek ve karşılaştırmak için kullanılır. *Gerekçe:* kullanıcı kararı. Devirdeki K-02 ("Excel ana model kalır, zincir otomatikleştirilir") bu kolda geçerli değildir.
  - *Not:* İlk talimatın md. 23'üyle (uzun vadeli vizyon: Planned → Model Alt → ana model otomatik güncellenir) ilişkisi kullanıcıya soruldu.
  - yerine geçer: 24.11.2026 – "STAR gibi" hedef geçerlidir; md. 23'ün vizyonu (Excel zincirinin otomatik güncellenmesi) bu kolda geçmez. *Gerekçe:* kullanıcı kararı.
- **İki kol:** Petkim'in tümden gelim kolu (ana modeli tanıtıp modelden sonuca giden ayrı repo) vardır. Repo adı ve birleşme uyumu kullanıcıya soruldu. *Gerekçe:* kullanıcı cevabı.
  - yerine geçer: 24.11.2026 – tümden gelim kolu "Petkim Weekly Forecast Automation - Engine" adıyla yürüyor (kullanıcının verdiği ad). GitHub repo adı ve birleşme uyumu (başlıklar, tarih biçimi) henüz cevaplanmadı.
  - yerine geçer: 24.11.2026 – tümden gelim kolunun GitHub reposu `petkim-weekly` (kullanıcı "petkim weekly" yazdı; tireli yazım teyit edilmedi). Başlıklar ve tarih biçimi (GG.AA.YYYY) birleşme için o kolla uyumlu tutulur. *Gerekçe:* kullanıcı cevabı ("olabilir").

## İlk talimat (md. 1–32) (24.11.2026)

- İlk talimatın metni (devir paketinde `A_Ilk_Talimat_Bolum1_md1-24.txt`, `B_Ilk_Talimat_Bolum2_md25-32.txt`) repoya girmez. Maddeler kullanıcıya tek tek teyit ettirilir; kalıcı kural `CLAUDE.md`'ye, karar bu günlüğe yazılır. Sade yapı korunur: md. 26'daki ayrı kayıtlar (Business Rule Register, Change/Exception/Assumption Log, Data Dictionary) açılmaz. *Gerekçe:* kullanıcı kararı.
- Ayıklama henüz başlamadı; hiçbir madde şu an kural sayılmaz.
- Ayıklama toplu turda yapılmaz; önce toplantıda input'lar tanıtılır (24.11.2026). *Gerekçe:* kullanıcı kararı.
- **Skill'ler:** İlk skill (`petkim-girdi-tanitma`) ilk input tanıtıldıktan sonra, yaşanan adımlar kullanıcıya onaylatılarak yazılır. *Gerekçe:* kullanıcı kararı.

## Tanıtım turu (24.11.2026)

- **Dönem:** Toplantıda tanıtılan dosyalar Kasım 2026 Planned dönemindendir; farklı dönemden gelen dosya yazılmadan önce kullanıcıya bildirilir. *Gerekçe:* kullanıcı kararı.
- **Önce göster, sonra yaz:** Tanım dosyasına yazılacak içerik önce sohbette gösterilir; kullanıcı onayından sonra repoya girer. *Gerekçe:* kullanıcı kararı.
- **Devirden kalan açık sorular (S-01…S-19):** İlgili dosya tanıtılırken, o dosyayı ilgilendirenler ekibe sorulmak üzere öne getirilir. *Gerekçe:* kullanıcı kararı.
- **RAW ve Planned çiftleri:** Kullanıcı tercih belirtmedi. Claude'un seçimi: iki ayrı tanım dosyası (`<ad>_RAW.md`, `<ad>_Planned.md`); RAW → Planned dönüşümü Planned tarafında yazılır. *Gerekçe:* "input başına tek dosya" kuralı ve girdi listesindeki satırlarla birebir eşleşme. Kullanıcı isterse değişir.
- **Tur 1 soru paneli:** Eski çalışmada incelenen yedi dosyadan (Forecast RAW/Planned, Hammadde RAW/Planned, Model Alt, ana model, Financial Results) kalan açık sorular ve üç genel soru panelde toplandı (31 soru): https://claude.ai/artifact/Gn4D82qQUQnFFTSTF8YtwU. Cevaplar panelden okunur; onaylanan kayda, cevapsız kalan `ACIK_SORULAR.md`'ye gider. *Gerekçe:* kullanıcı talebi; toplantıda ekiple cevaplanacak.
- **Tur 1 cevapları alındı (24.11.2026):** 31 sorunun 27'si toplantıda cevaplandı; 4'ü "sonra cevaplanacak" (G1-21'in grubu, I457 UV ve S 00356 YY, Büten birimi, Toluen+Reformat), 1'inin cevabı eksik (Planned'da olup RAW'da olmayan ürünler). Panel ikinci tura güncellendi (aynı adres): açık kalan 5 soru, cevaplardan doğan 7 yeni soru ve Claude'un cevaplardan anladığının 15 maddelik teyidi. Cevaplardan çıkan kararlar teyit turundan sonra bu günlüğe ve `CLAUDE.md`'ye işlenir. *Gerekçe:* varsayımla devam edilmez; notla verilen cevapların yorumu teyit edilmeden kural olmaz.

## Tur 1 panel cevapları (24.11.2026)

Toplantıda Petkim ekibiyle panelde verilen cevaplar. *Gerekçe (hepsi için):* panel cevabı; parantez içindeki kod panel sorusudur. Kişi adları buraya yazılmadı; yalnız ekip adı tutulur.

**Kapsam ve dönem**
- Kapsam yalnız verilen forecast ayıdır (örnekte Kasım). Forecast ayı dışındaki aylarla ilgilenilmez; tek istisna stoktur. (M1)
- Yılın kalan aylarını içeren aylık n+m verisinden (ör. 10+2) yalnız ilgili ay kullanılır. (F2)
- "Planned" bir dosya türü değil, periyoda verilen addır; ada anlam yüklenmez. Haftalığın ilk çalışması 0+30/31'dir; Planned aylık çalışmayı baz alır. (G1)
- Çıktı yalnız son versiyondan üretilir. v2, CFO yorumlarından sonra yapılan güncellemedir ve her hafta oluşmaz; ilk versiyon klasörü karşılaştırma için bilerek tutulur. (G5)
- Haftalık çalışmada yalnız P&L forecast'i çıkarılır. Forecast ayını etkilemeyen geçmiş ayın P&L'sinin boş olması sorun değildir. (A3)

**Stok**
- Her çalışma stokludur. Önceki ayın kapanış stoğu yetiştiyse forecast çalışılan aydan başlar; yetişmediyse bir önceki aydan başlatılır ve aradaki aya forecast verisi girilerek o ayın kapanış stoğu tahmin edilir. (G2)
- Ticari ürünler stoksuz çalışılır: alış miktarı her zaman satış miktarına eşittir; aksi olursa ekip bildirir. (F10)

**Birimler ve ürünler**
- Temel birimler: miktar ton, fiyat USD/ton, Results tutarı USD mn. (G3)
- Üretimden satış ürünleri (Financial Results'taki adlarıyla): Etilen, Aromatik Yağ, Py-Gas, PS Propilen (PSP), KS Propilen (KSP), C4, Benzen, C5 Karışımı, Toluen, Ortoksilen, Ağır Arom, Paraksilen, Naphtha-Aromatic, ACN, Reformate, MEG, AYPE, AYPE-T, YYPE, PP, PTA, PA, Kostik, PVC. Ticari ürünler sabit liste değildir; Forecast verisinin ticari ürün bölümünde ne varsa odur. (G4)

**Girdiler**
- Forecast RAW DATA haftalık gelir; ticaret ekibi hazırlar. (F1) Haftalık dosyanın yapısı aylıkla aynıdır, küçük değişiklikler olabilir; yapı dosya geldikçe öğrenilir, soru varsa sorulur. (F2)
- Hammadde Planı RAW DATA haftalık gelir; planlama ekibi hazırlar. (H1)
- İthal nafta fiyatı sabit bir kuralla üretilmez; her çalışmada girdi olarak verilir (beklenen kaynak planlama ekibi, bazen Daily Prices'a göre güncellenir). Farklı versiyon çalışılırsa ekip bildirir. (H2)
- STAR nafta miktarının esas kaynağı STAR Financial Model'dir. (H3)
- "STAR nafta fiyatı = ithal nafta fiyatı + sabit prim" kuralı geçerli değildir. (H4) Fiyatın nasıl belirlendiği açık (`ACIK_SORULAR.md`).
- PS Propilen alış fiyatı PGP fiyatına eşit alınır. PGP adı sonra güncellenecek. (H6)
- PETKİM&STAR Gas Power Prices: Model Alt Çalışması bu dosyadan beslenir; doğalgaz ve elektrik fiyat tahminlerini içerir. Bazen güncellenmez ve önceki haftanın verisi gönderilir; bu sorun sayılmaz. (kullanıcı, 24.11.2026 sohbet)
- STAR payı STAR Results dosyasından %12 oranıyla alınır. (R3)

**Ürün eşleme**
- RAW'daki bütün ürünlerin sonuca akması beklenir. Yeni ürün doğru stok ve maliyet yapısıyla ilişkilendirilir; modeldeki bağlantı sistemi anlaşılarak sonuca yansıtılır. (F7) Planned'da olup RAW'da olmayan ürünler için de aynı cevap bilerek verildi: belirleyici olan RAW'dır. (F8; kullanıcı teyidi 24.11.2026)
- RAW'daki AG 251 ile Planned'daki FH360 PP farklı ürünlerdir. (F6)
- Tamlık kontrolünü (RAW'daki her ürün Planned'da var mı) Claude yapar. Planned'daki kontrol kolonları bu amaçladır ve şu an bozuktur. (F9)

**Model hataları ve elle değerler**
- Modelde hata ya da mantıksızlık görülürse Claude kendisi düzeltmez, ekibi uyarır. (F7)
- Hata olarak teyit edilenler: HDPE grubundaki "EC 281 MB" etiketli satırın METHANOL satırını okuması (F4); ticari ürünlerdeki satır kayması ve çift sayım, "isimler düzeltilmeli" (M2).
- Elle düzeltme normalde beklenmez; gerekirse ekip bildirir. (A1) Results'taki elle düzeltmelerin hepsi ekipçe açıklanacak; Claude'dan çözmesi beklenmez ama gördüğünü mutlaka bildirir. Upside/Downside dosyası ayrıca tanıtılacak. (R1) "CHECK with MODEL" farkı bu elle müdahalelerden gelir. (R2)
- Forecast ayında hata yoksa model kontrolündeki diğer aylara ait hatalar görmezden gelinebilir. (A2)
- Model Alt'taki 2025 dosyalarına giden eski bağlantılar bilerek durur; bütçeden kalan sabit yapıdır. (M4)

**Açık kalanlar** `ACIK_SORULAR.md`'ye taşındı: G1-21'in grubu (F3), I457 UV ve S 00356 YY (F5), Büten birimi (H5), Toluen + Reformat (M3).

## Dosyaların yeniden okunması ve tur 3 paneli (24.11.2026)

- **Toplantı notu:** Kullanıcının ilettiği toplantı notu talimat sayılmaz; yalnız okunur. Nottan çıkan gözlemler panelde sorulur, cevaba göre kayda girer. *Gerekçe:* kullanıcı talimatı.
- **Okunan dosyalar:** Kasım 2026 Planned (v2) klasöründen on dosya: Forecast RAW ve Planned, Hammadde Planı RAW ve Planned, Üretim Planı RAW ve Planned, Gas Power Prices, Model Alt Çalışması, ana model, Financial Results. Üretim Planı ve Gas Power Prices ilk kez okundu. `GIRDI_LISTESI.md` durumları güncellendi.
- **Tur 3 paneli (aynı adres):** 16 soru sonraki toplantıda Petkim ekibine, 6 soru toplantı notundan çıkan gözlem olarak kullanıcıya. Sorular `ACIK_SORULAR.md` #4–#26'da; dosyadaki gözlemle tam metin panelde.
- **Tanım dosyaları henüz yazılmadı:** "önce göster, sonra yaz" kuralı gereği taslaklar sırayla sohbette gösterilecek.

## Nihai çıktı: yönetim sunumu (26.11.2026)

- **Nihai hedef sunumdur.** Proje sonunda girdiler tanıtıldığında Petkim için haftalık RPBU Management Meeting sunumunun Petkim slaytları üretilebilmelidir. Yönetimin bildiği ve anladığı format budur; dashboard da mutlaka bu verileri göstermelidir. *Gerekçe:* kullanıcı kararı. İncelenen dosyalar: `PETKIM_STAR_Weekly_Forecast_Update_Presentation_<Ay>_Planned.xlsm` (sunum besleme dosyası) ve `Management meeting template_<GG.AA.YYYY>.pptx`. Dosyalar repoya girmez.
- **Kapsam yalnız Petkim.** Hedef slaytlar (besleme dosyasındaki sayfa adıyla):
  - **S07 Petkim EBITDA (mUSD):** P&L tablosu — Production Revenue, Raw Material, Utility, Production Base Profit, Operating Cost (Personnel / Non-personnel), Production EBITDA, Trade Revenue, Trade Cost, Trade GP, Trade Operating Cost (Personnel / Non-personnel), Trade EBITDA, STAR Net income contribution, Total EBITDA, Total EBITDA (year-end forecast). Üç KPI kartı: toplam EBITDA, Production EBITDA (+Trade EBITDA), STAR katkısı (Petkim EBITDA içindeki payı).
  - **S08 Hammadde (ton, USD/t):** tüketim ve satın alma tabloları (Naphtha Light, Naphtha Heavy, Imported Ethylene, Reformate, Total & Weighted Average; miktar ve birim maliyet); Etilen tablosu (ithal fiyat, üretim maliyeti, ağırlıklı ortalama, Ethylene Charging ton/saat). İki KPI kartı: ağırlıklı tüketim maliyeti, etilen üretim maliyeti.
  - **S09 Üretim ürünleri satışı (ton, USD/t):** gruplar Polymers (LDPE, LDPE-T, HDPE, PP), Aromatics (Benzene, C5 Mixture, Toluene, Reformate, Paraxylene, Naphtha–Aromatic), Plastics (PA, PVC), Ethylene (Ethylene, Aromatic Oil, C4, PSP), Other (ACN); grup toplamları ve Grand Total. Kolonlar: satış hacmi, birim satış fiyatı, nafta üstü marj (her biri LF / Budget / Change).
  - **S10 Ticari ürünler (ton, kUSD):** ürün bazında satış hacmi ve brüt kâr (LF / Budget / Change), Total. İki KPI kartı: ticari brüt kâr, ticari hacim.
  - **S02 R&P BU EBITDA'daki Petkim satırları:** ay ve yıl sonu "Petkim (incl. STAR contribution)" ile "STAR contribution (12% share)". Diğer şirket satırları (STAR, Petrol Ticaret, STAD, AR-GE) ve makro tablo bu kolun kapsamı dışında.
- **Format kuralları (sunumdan okunan):** Kolon düzeni "<Ay YYYY> Latest Forecast | <Ay YYYY> Budget | Change | Change %"; P&L'de ayrıca "2025 Actual Average". Change % için kural: bütçe 0 ise "n.m.", oran mutlak değerce 10'u aşarsa "n.m.". Rakam biçimi Türkçe (binlik nokta, ondalık virgül), negatif parantez içinde. Slayt başlığı "Petkim EBITDA Performance – <Ay> Forecast (<birim>)". Kart birimleri sunumda sabittir. Besleme dosyasında tanımlı adlar sunumdaki şekil adlarıyla aynıdır (S07_T1, S07_KV1 …); makro (`SunumaAktar`) yalnız metni ve yazı rengini taşır.
- **Mevcut zincir (gözlem, karar değil):** Petkim slaytları `Petkim Waterfall Forecast Vs Budget_<yıl>_<n m> <Ay> Planned.xlsx` dosyasından (sayfalar: PETKIM PL Details, Raw Materials, Etilen Charge, Production Sales, Trade Goods) okunuyor; bütçe kolonu bu dosyanın içinde. S02'deki Petkim bütçesi `2026 Budget_Financial Results_65USD Brent` dosyasından, yıl sonu STAR katkısı aylık 9+3 Financial Results ile Planned v2 Financial Results'tan okunuyor. Gözlemler `ACIK_SORULAR.md` #27–#31'de.
- **Sunumun diğer slaytları** (STAR slaytları, STAR entegrasyonu, stok seviyeleri, yaptırımlar, proje/hedge, ek bütçe talebi, nakit akışları) haftalık forecast çıktısı sayılmadı; stok slaytlarının kapsamı açık soru (#30).

