# Petkim Weekly Forecast — Tümevarım

> **Durum: İLK TASLAK (24.11.2026).** "Taslak – kullanıcıya sorulacak" işaretli bölümler henüz karara bağlanmadı; cevap gelene kadar boş kalır.

Petkim haftalık forecast'ının tümevarım kolu: forecast'a giren input dosyaları tek tek tanıtılır; her birinin yapısı, hangi alanın neye yaradığı ve forecast'a nasıl bağlandığı kayda geçirilir. Bu dosya projenin giriş noktası: her oturum önce bunu, sonra `KARAR_GUNLUGU.md`'yi okur.

## İlkeler

1. **Varsayımla devam edilmez.** Kullanıcının cevaplamadığı hiçbir konu kabul sayılmaz. Claude önerisini söyleyebilir; karar kullanıcınındır.
2. **Emin olunmayan konu açık soru olur.** Petkim ekibinin bilmesi gereken konu "Petkim ekibine sorulacak" diye işaretlenir ve `ACIK_SORULAR.md`'ye eklenir. Bu sorular kullanıcı ve Petkim ekibiyle birlikte cevaplanır.
3. **Soru-cevap düzeni.** Her seferinde en fazla 3–4 soru sorulur; mümkünse seçenekli.

## Bilgi nerede durur

| Bilgi | Yeri |
|---|---|
| Kalıcı kurallar: klasör yapısı, isimlendirme, birimler, dönem tanımları, input tanıtım şablonu | `CLAUDE.md` (bu dosya) |
| Alınan kararlar (tarih + kısa gerekçe) | `KARAR_GUNLUGU.md` |
| Açık sorular (Petkim ekibine sorulacaklar dahil) | `ACIK_SORULAR.md` |
| Input tanımları | `inputs/<dosya_adı>.md` (input başına tek dosya) |
| Tanıtılan dosyanın kendisi ve şirket verisi | Sohbete eklenir; repoya girmez (`.gitignore`) |

## Klasör yapısı

```
CLAUDE.md
KARAR_GUNLUGU.md
ACIK_SORULAR.md
inputs/
```

## İsimlendirme

*Taslak – kullanıcıya sorulacak.*

## Birimler

*Taslak – kullanıcıya sorulacak.*

## Dönem tanımları

*Taslak – kullanıcıya sorulacak.*

## Petkim yapısı

*Taslak – kullanıcıya sorulacak* (birimler, ürünler, forecast ufku, input listesi).

## Input tanıtım şablonu

Her input için `inputs/<dosya_adı>.md` açılır. Başlıklar:

- **Kaynak**
- **Sahibi**
- **Güncellenme sıklığı**
- **Sayfa / kolon yapısı**
- **Birimler**
- **Forecast'teki kullanımı**
- **Açık sorular** (ayrıca `ACIK_SORULAR.md`'de listelenir)

## Oturum rutini

**Başlangıç**
1. Repoyu oturuma ekle ve klonla (klonluysa `git pull --rebase`).
2. `CLAUDE.md`, ardından `KARAR_GUNLUGU.md` oku.

**Bitiş**
1. Oturumda alınan kararları tarih ve kısa gerekçeyle `KARAR_GUNLUGU.md`'ye yaz.
2. Değişiklikleri commit'le ve push'la.
3. Neyin değiştiğini kullanıcıya iki üç cümleyle özetle.

## Dil

Türkçe.
