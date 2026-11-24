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
