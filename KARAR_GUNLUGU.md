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
