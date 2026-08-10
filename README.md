# handebalci-web

Av. Hande Balcı için tek sayfalık, iki dilli (TR/EN) tanıtım sitesi.
Saf HTML/CSS — framework yok, client-side JS yok, harici istek yok.

- **TR:** `/` (varsayılan)
- **EN:** `/en/`
- Hedef adres: **https://handebalci.av.tr** (alan adı henüz bağlanmadı)

## Yerelde çalıştırma

```bash
python3 -m http.server 8080
```

http://localhost:8080 adresini açın.

## Yayın (GitHub Pages)

Repo: `anunnaki-cosmo-crew/handebalci-web`. Pages, `main` branch kökünden yayınlanır;
site alan adı bağlanana kadar `https://anunnaki-cosmo-crew.github.io/handebalci-web/`
altında çalışır (tüm linkler göreli olduğu için alt path sorun çıkarmaz).

## Alan adını bağlama (handebalci.av.tr)

`.av.tr` uzantısı yalnızca baro levhasına kayıtlı avukatlara tahsis edilir —
tescili Hande Balcı'nın kendi adına (TRABİS akredite bir kayıt operatörü
üzerinden, baro kimliğiyle) yapması gerekir.

Alan adı alındıktan sonra:

1. Köke `CNAME` dosyası ekleyin (içeriği tek satır: `handebalci.av.tr`) ve push edin.
   (Dosya bilerek şimdiden eklenmedi: CNAME mevcutken Pages, henüz çözümlenmeyen
   alan adına yönlendirir ve github.io önizlemesi kırılır.)
2. DNS'te şu kayıtları oluşturun:
   - `handebalci.av.tr` → **A** kayıtları: `185.199.108.153`, `185.199.109.153`,
     `185.199.110.153`, `185.199.111.153`
   - `www.handebalci.av.tr` → **CNAME**: `anunnaki-cosmo-crew.github.io` (isteğe bağlı)
3. Repo → Settings → Pages → Custom domain alanına `handebalci.av.tr` yazın ve
   **Enforce HTTPS**'i işaretleyin (sertifika birkaç dakika içinde kesilir).

## E-posta

`info@handebalci.av.tr` — alan adı alındıktan sonra bir e-posta sağlayıcısında
(ör. Yandex 360, Zoho Mail, Google Workspace) kurulacak; MX kayıtları DNS'e eklenecek.

## İçerik güncelleme

Gerçek bilgiler geldikçe `[KÖŞELİ PARANTEZ]` içindeki placeholder'lar değiştirilecek —
tam liste `CLAUDE.md` içinde.
