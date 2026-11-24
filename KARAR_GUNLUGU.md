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
