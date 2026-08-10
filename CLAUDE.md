# handebalci-web

Av. Hande Balcı'nın kişisel avukatlık sitesi. Tek sayfa, TR (`/`) + EN (`/en/`),
saf HTML/CSS, GitHub Pages. Hedef adres `handebalci.av.tr` (bağlama adımları README'de).

## Hard rules

- **Sıfır client-side JS, harici istek yok.** Font, analytics, CDN, çerez, izleme yok.
  Dil anahtarı iki statik sayfa arasındaki linktir.
- **Tüm linkler göreli.** Site hem `github.io/handebalci-web/` alt path'inde hem custom
  domain kökünde çalışmalı — asla `/` ile başlayan mutlak path yazma.
- **Reklam yasağına uygunluk.** İçerik TBB meslek kurallarına uygun, bilgilendirme
  amaçlı kalmalı; "en iyi", "kazandırır" gibi reklam/övgü dili kullanma. Footer'daki
  bilgilendirme notunu kaldırma.
- **İki dil senkron.** `index.html`'de yapılan her içerik değişikliği `en/index.html`'e
  de yansıtılmalı (ve tersi).
- **CNAME dosyasını alan adı tescil edilmeden ekleme** — Pages'i ölü domaine yönlendirir.

## Placeholder listesi

Gerçek bilgi geldikçe `[KÖŞELİ PARANTEZ]` içindekiler değiştirilecek (iki dilde birden):

| Placeholder | Neresi |
|---|---|
| `[TAGLINE]` | Hero alt başlığı |
| `[ÜNİVERSİTE]` / `[UNIVERSITY]` | Hakkında |
| `[BARO]` / `[BAR]` | Hakkında |
| `[ŞEHİR]` / `[CITY]` | Hakkında, meta description |
| `[DENEYİM]` / `[EXPERIENCE]` | Hakkında 1. paragraf |
| `[İKİNCİ PARAGRAF]` / `[SECOND PARAGRAPH]` | Hakkında 2. paragraf |
| `[+90 5XX XXX XX XX]` | İletişim telefonu (`tel:` href'i de güncellenmeli) |
| `[OFİS ADRESİ]` / `[OFFICE ADDRESS]` | İletişim adresi |
| Çalışma alanları kartları | 6 alan varsayılan/geçici — Hande Balcı'nın gerçek alanlarıyla doğrulanacak |

## Conventions

- Stil tek dosyada: `assets/style.css`. Renk/tipografi token'ları `:root`'ta.
- Trunk-based; küçük site olduğu için doğrudan `main`'e push kabul edilir.
