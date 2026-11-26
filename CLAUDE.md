# Petkim Weekly Forecast — Tümevarım

> **Durum: İLK TASLAK (24.11.2026).** "Taslak – kullanıcıya sorulacak" işaretli bölümler henüz karara bağlanmadı; cevap gelene kadar boş kalır.

Petkim haftalık forecast'ının tümevarım kolu: forecast'a giren input dosyaları tek tek tanıtılır; her birinin yapısı, hangi alanın neye yaradığı ve forecast'a nasıl bağlandığı kayda geçirilir. Bu dosya projenin giriş noktası: her oturum önce bunu, sonra `KARAR_GUNLUGU.md`'yi okur.

## Anayasa (kullanıcı, 26.11.2026)

Kullanıcının "anayasa olarak al" dediği kurallar. Diğer bütün kuralların üstündedir; yalnız kullanıcı değiştirir.

1. **Claude kendisi karar vermez.** Rakamlar ya da konular hakkında Claude kendisi karar vermez; dosyadan okuduğu yorumu kural gibi kayda yazmaz.
2. **Sorun varsa tekrar sorar.** Cevap belirsizse ya da yeni bir sorun çıkarsa Claude yeniden sorar; cevapsız soru açık soru olarak kalır, varsayımla kapatılmaz.
3. **Çıktıyı Claude üretir.** Girdiler verilir; Claude bunlardan modeli, ara çıktıları ve sunumu üretir. Sunum besleme Excel'i gönderilmez.
4. **Nihai hedef Petkim yönetim sunumudur.** Yönetimin bildiği ve anladığı format budur; bu kolda yapılacak dashboard da bu verileri göstermelidir.

## İlkeler

1. **Varsayımla devam edilmez.** Kullanıcının cevaplamadığı hiçbir konu kabul sayılmaz. Claude önerisini söyleyebilir; karar kullanıcınındır. Claude rakamlar ya da konular hakkında kendisi karar vermez; dosyadan okuduğunu kural gibi kayda yazmaz, sorar (26.11.2026). Cevapsız kalan soru açık soru olarak kalır.
2. **Emin olunmayan konu açık soru olur.** Petkim ekibinin bilmesi gereken konu "Petkim ekibine sorulacak" diye işaretlenir ve `ACIK_SORULAR.md`'ye eklenir. Bu sorular kullanıcı ve Petkim ekibiyle birlikte cevaplanır.
3. **Soru-cevap düzeni.** Her seferinde en fazla 3–4 soru sorulur; mümkünse seçenekli.
4. **Model doğru cevap sayılmaz; hata düzeltilmez, bildirilir.** Modelde hata ya da mantıksızlık görülürse Claude kendisi düzeltmez, ekibi uyarır. Elle girilmiş değer görülürse kaynağı sorulur; elle düzeltme uydurulmaz.
5. **Rakam yazılmaz.** `inputs/` dosyalarına, skill'lere ve listelere gerçek rakam ya da şirket verisi yazılmaz; yalnız yapı ve anlam.

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
- RAW DATA ve Planned çiftleri iki ayrı tanım dosyasıdır (`<ad>_RAW.md`, `<ad>_Planned.md`); RAW → Planned dönüşümü Planned tarafında yazılır.
- Dosyanın gerçek ad kalıbı (dönemin nasıl yazıldığı dahil) tanım dosyasının içinde yazılır.

## Birimler

- Miktar **ton**, fiyat **USD/ton**, Financial Results tutarı **USD mn**.
- Bu kuraldan sapan birim (ör. KG etiketi) ilgili input'un tanım dosyasında yazılır ve teyit edilene kadar açık sorudur.

## Dönem tanımları

- **Kapsam yalnız verilen forecast ayıdır.** Forecast ayı dışındaki aylarla ilgilenilmez; tek istisna stoktur.
- Yılın kalan aylarını içeren aylık n+m verisinden (ör. 10+2) yalnız ilgili ay kullanılır.
- **"Planned" periyoda verilen addır**, dosya türü değildir. Dosya ve klasör adına anlam yüklenmez; dönem dosyanın içeriğinden okunur.
- Haftalığın ilk çalışması 0+30/31'dir. Periyot adlarının tam sırası açık (`ACIK_SORULAR.md`).
- **Versiyon:** çıktı yalnız son versiyondan üretilir. v2, CFO yorumlarından sonra yapılan güncellemedir; her hafta oluşmaz.
- **Stok:** her çalışma stokludur. Önceki ayın kapanış stoğu yetiştiyse forecast çalışılan aydan başlar; yetişmediyse bir önceki aydan başlatılır ve aradaki ayın kapanış stoğu forecast verisiyle tahmin edilir. Ticari ürünler stoksuzdur: alış miktarı = satış miktarı.
- Haftalık çalışmada yalnız P&L forecast'i çıkarılır.

## Petkim yapısı

- **Üretimden satış ürünleri** (Financial Results'taki adlarıyla): Etilen, Aromatik Yağ, Py-Gas, PS Propilen (PSP), KS Propilen (KSP), C4, Benzen, C5 Karışımı, Toluen, Ortoksilen, Ağır Arom, Paraksilen, Naphtha-Aromatic, ACN, Reformate, MEG, AYPE, AYPE-T, YYPE, PP, PTA, PA, Kostik, PVC.
- **Ticari ürünler** sabit liste değildir; Forecast verisinin ticari ürün bölümünde ne varsa odur.
- **RAW belirleyicidir:** RAW'daki bütün ürünlerin sonuca akması beklenir. Yeni ürün doğru stok ve maliyet yapısına bağlanır; hangi yapıya bağlanacağı sorulur, tahmin edilmez.
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

**Önce göster, sonra yaz:** Tanım dosyasına yazılacak içerik önce sohbette gösterilir; kullanıcı onayından sonra repoya girer. Teyitsiz her şey "Açık sorular"da durur.

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
- **Birleşme uyumu:** Tümden gelim kolu `petkim-weekly` reposudur ("Petkim Weekly Forecast Automation - Engine"). Başlıklar ve tarih biçimi (GG.AA.YYYY) onunla uyumlu tutulur.
- **Devir paketi:** Eski hesaptaki Petkim çalışması (20.11.2026 devir paketi) yalnız arka plan bilgisidir; ondan bir şey ancak kullanıcı teyidiyle kayda girer (`KARAR_GUNLUGU` "Devir paketi").

## Dil

Türkçe.
