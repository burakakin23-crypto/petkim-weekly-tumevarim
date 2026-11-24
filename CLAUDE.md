# Petkim Weekly Forecast — Tümevarım

> **Durum: İLK TASLAK (24.11.2026).** "Taslak – kullanıcıya sorulacak" işaretli bölümler henüz karara bağlanmadı; cevap gelene kadar boş kalır.

Petkim haftalık forecast'ının tümevarım kolu: forecast'a giren input dosyaları tek tek tanıtılır; her birinin yapısı, hangi alanın neye yaradığı ve forecast'a nasıl bağlandığı kayda geçirilir. Bu dosya projenin giriş noktası: her oturum önce bunu, sonra `KARAR_GUNLUGU.md`'yi okur.

## İlkeler

1. **Varsayımla devam edilmez.** Kullanıcının cevaplamadığı hiçbir konu kabul sayılmaz. Claude önerisini söyleyebilir; karar kullanıcınındır.
2. **Emin olunmayan konu açık soru olur.** Petkim ekibinin bilmesi gereken konu "Petkim ekibine sorulacak" diye işaretlenir ve `ACIK_SORULAR.md`'ye eklenir. Bu sorular kullanıcı ve Petkim ekibiyle birlikte cevaplanır.
3. **Soru-cevap düzeni.** Her seferinde en fazla 3–4 soru sorulur; mümkünse seçenekli.
4. **Rakam yazılmaz.** `inputs/` dosyalarına, skill'lere ve listelere gerçek rakam ya da şirket verisi yazılmaz; yalnız yapı ve anlam.

## Bilgi nerede durur

| Bilgi | Yeri |
|---|---|
| Kalıcı kurallar: klasör yapısı, isimlendirme, birimler, dönem tanımları, input tanıtım şablonu | `CLAUDE.md` (bu dosya) |
| Alınan kararlar (tarih + kısa gerekçe) | `KARAR_GUNLUGU.md` |
| Açık sorular (Petkim ekibine sorulacaklar dahil) | `ACIK_SORULAR.md` |
| Input tanımları | `inputs/<dosya_adı>.md` (input başına tek dosya) |
| Girdi kontrol listesi (hangi input var, durumu) | `GIRDI_LISTESI.md` |
| İş sıraları ve bakış açıları | `skills/` (katalog: `skills/README.md`) |
| Tanıtılan dosyanın kendisi ve şirket verisi | Sohbete eklenir; repoya girmez (`.gitignore`) |

## Klasör yapısı

```
CLAUDE.md
KARAR_GUNLUGU.md
ACIK_SORULAR.md
GIRDI_LISTESI.md
inputs/
skills/
  README.md
```

## İsimlendirme

- `inputs/` altındaki tanım dosyasının adı **dönemsiz sabit addır**: dosya adındaki dönem, tarih ve sürüm kısmı atılır, boşluk ve Türkçe karakter sadeleştirilir (ör. `Hammadde Planı 10 2 11.2026_RAW DATA.xlsx` → `inputs/Hammadde_Plani_RAW.md`). Her hafta aynı tanım dosyası güncellenir.
- Dosyanın gerçek ad kalıbı (dönemin nasıl yazıldığı dahil) tanım dosyasının içinde yazılır.

## Birimler

Ölçü birimleri (miktar, fiyat, tutar, para birimi). Ekipten cevap bekleniyor (`ACIK_SORULAR.md` #2); o zamana kadar birim her input tanıtılırken o dosya için teyit edilir.

## Dönem tanımları

Ekipten cevap bekleniyor (`ACIK_SORULAR.md` #1).

## Petkim yapısı

- **Ürünler ve ürün grupları:** ekipten cevap bekleniyor (`ACIK_SORULAR.md` #3).
- **Forecast ufku:** "Dönem tanımları"na bakınız.
- **Input listesi:** `GIRDI_LISTESI.md`.

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

## Çalışma düzeni

- **Git:** Tek dal, `main`. Değişiklik doğrudan `main`'e gider; açık dal bırakılmaz.
- **Eşzamanlı çalışma:** Aynı anda iki oturum çalışabilir.
  - Her yazmadan hemen önce `git pull --rebase`.
  - Değişiklik küçük commit'lerle hemen push edilir.
  - Dosya baştan yazılmaz; yalnız ilgili satır eklenir ya da değiştirilir (özellikle `KARAR_GUNLUGU.md`).
  - Push reddedilirse yeniden `git pull --rebase`.
  - Çakışmada diğer kişinin satırı silinmez; iki satır birleştirilir. Anlamca çelişiyorsa kullanıcıya sorulur.
- **Devir paketi:** Eski hesaptaki Petkim çalışması (20.11.2026 devir paketi) yalnız arka plan bilgisidir; ondan bir şey ancak kullanıcı teyidiyle kayda girer (`KARAR_GUNLUGU` "Devir paketi").

## Dil

Türkçe.
