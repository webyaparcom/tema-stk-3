# tema-stk-3 · k8il01 — İlan Filtre (Emlak İlan Listesi)

## Nedir

tema-stk-3 sitesinin matrix modülü. `İlan Filtre (Emlak İlan Listesi)` şablonu (section kökü,
sınıf `modulex-ilan`) render sırasında sitenin sayfa akışına eklenir. Şablon içeriği
`index.html`'deki `{{...}}` soketleriyle, veri/tema değerleri `index.json`'la
beslenir.

## Dosyalar

| Dosya | Rol |
|-------|-----|
| `back.js` | Modül davranışı (vanilla JS) (13 KB) |
| `index.html` | Modül şablonu (render hedefi) (27 KB) |
| `index.json` | Veri + tema token'ları (10 KB) |

## Girdiler
| Değişken | Örnek değer |
|--------|-------------|
| `max` | `1200px` |
| `bgcolor` | `var(--mx-site-bg, #ffffff)` |
| `textcolor` | `var(--mx-site-text, #1b1b1b)` |
| `mutedcolor` | `color-mix(in srgb, var(--mx-site-text, #1b1b1b) 72%, var(--mx-site-bg, #fff))` |
| `surface` | `var(--mx-site-surface, #f6f6f4)` |
| `surface2` | `var(--mx-site-surface-2, #ececea)` |
| `accent` | `var(--mx-site-primary, #2563eb)` |
| `accentText` | `var(--mx-site-primary-contrast, #ffffff)` |

- `name`: `İlan Filtre (Emlak İlan Listesi)`
- `data`: 3 kayıt. Örnek: `{"facets": ["type", "rooms", "m2", "price", "district"], "typeLabels": {"daire": {"tr": "Daire", "en": "Apartment", "ar": "شقة"}, "villa": …`
- Diğer anahtarlar: `description`, `version`, `icon`, `category`, `tags`

## Temaya bağımlılık
Tema token'ları `index.json -> desing` üzerinden gelir (önceki tablo): **max**, **bgcolor**, **textcolor**, **mutedcolor**, **surface**.

## Test

Webmaker render hattında site sayfası üretilir; çıktı HTML'de bu modülün kök bloğu
(`modulex-ilan`) yerleşik görünmelidir. Render ucu: mcp/webmaker
render aracı / proje site dizini çıktısı.

## Kullanım örneği

Modül tema-stk-3 sitesinde `web/matrix/modules/k8il01/` yolunda tanımlıdır; sayfa
yapılandırması bu yolu referans alır. Veri örneği (`index.json`):
```
{
  "name": "İlan Filtre (Emlak İlan Listesi)",
  "desing": {
    "max": "1200px",
    "bgcolor": "var(--mx-site-bg, #ffffff)",
    "textcolor": "var(--mx-site-text, #1b1b1b)",
    "mutedcolor": "color-mix(in srgb, var(--mx-site-text, #1b1b1b) 72%, var(--mx-site-bg, #fff))",
    "surface": "var(--mx-site-surface, #f6f6f4)",
    "surface2": "var(--mx-site-surface-2, #ececea)",
    "accent": "var(--mx-site-primary, #2563eb)",
    "accentText": "var(--mx-site-primary-contrast, #ffffff)",
    "bordercolor": "color-mix(in srgb, var(--mx-site-text, #1b1b1b) 18%, transparent)",
    "pageSize": 6,
    "sort": "date",
    "urlState": true,
    "title": {
      "tr": "Emlak İlanları",
      "en": "Pro
```

## Notlar

- Oluşturuldu: 2026-11-01 — modül envanterinde otomatik tamamlanan README (kaynak dosyalar: index.json, index.html).
- İçerik bu klasördeki gerçek dosyalardan okunarak yazıldı; modül değişikliğinde elden güncellenmelidir.
