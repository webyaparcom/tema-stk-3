# tema-stk-3 · k8hr01 — Hero 2 (Ortalanmış)

## Nedir

tema-stk-3 sitesinin matrix modülü. `Hero 2 (Ortalanmış)` şablonu (section kökü,
sınıf `modulex-hero2`) render sırasında sitenin sayfa akışına eklenir. Şablon içeriği
`index.html`'deki `{{...}}` soketleriyle, veri/tema değerleri `index.json`'la
beslenir.

## Dosyalar

| Dosya | Rol |
|-------|-----|
| `back.js` | Modül davranışı (vanilla JS) (0 KB) |
| `index.html` | Modül şablonu (render hedefi) (4 KB) |
| `index.jpeg` | Önizleme görseli (29 KB) |
| `index.json` | Veri + tema token'ları (1 KB) |

## Girdiler
| Değişken | Örnek değer |
|--------|-------------|
| `max` | `1200px` |
| `gradient` | `linear-gradient(150deg, #0f172a 0%, #1e3046 55%, #0f172a 100%)` |
| `glow1` | `rgba(222, 109, 38, 0.55)` |
| `glow2` | `rgba(33, 150, 243, 0.45)` |
| `btnbg` | `#B4521A` |
| `btncolor` | `#ffffff` |
| `badge` | `{'tr': 'Yeni Nesil Çözümler', 'en': 'Next Generation Solutions'}` |
| `title` | `{'tr': 'İşinizi Dijitalde Büyütün', 'en': 'Grow Your Business Digitally'}` |

- `name`: `Hero 2 (Ortalanmış)`
- Diğer anahtarlar: `category`, `description`, `version`, `icon`

## Temaya bağımlılık
Tema token'ları `index.json -> desing` üzerinden gelir (önceki tablo): **max**, **gradient**, **glow1**, **glow2**, **btnbg**.

## Test

Webmaker render hattında site sayfası üretilir; çıktı HTML'de bu modülün kök bloğu
(`modulex-hero2`) yerleşik görünmelidir. Render ucu: mcp/webmaker
render aracı / proje site dizini çıktısı.

## Kullanım örneği

Modül tema-stk-3 sitesinde `web/matrix/modules/k8hr01/` yolunda tanımlıdır; sayfa
yapılandırması bu yolu referans alır. Veri örneği (`index.json`):
```
{
  "name": "Hero 2 (Ortalanmış)",
  "desing": {
    "max": "1200px",
    "gradient": "linear-gradient(150deg, #0f172a 0%, #1e3046 55%, #0f172a 100%)",
    "glow1": "rgba(222, 109, 38, 0.55)",
    "glow2": "rgba(33, 150, 243, 0.45)",
    "btnbg": "#B4521A",
    "btncolor": "#ffffff",
    "badge": {
      "tr": "Yeni Nesil Çözümler",
      "en": "Next Generation Solutions"
    },
    "title": {
      "tr": "İşinizi Dijitalde Büyütün",
      "en": "Grow Your Business Digitally"
    },
    "description": {
      "tr": "Modern tasarım ve güçlü altyapıyla markanızı bir üst seviyeye taşıyın.",
      "en": "Take your brand to the next level with modern design and a strong infrastructure."
    },
  
```

## Notlar

- Oluşturuldu: 2026-11-01 — modül envanterinde otomatik tamamlanan README (kaynak dosyalar: index.json, index.html).
- İçerik bu klasördeki gerçek dosyalardan okunarak yazıldı; modül değişikliğinde elden güncellenmelidir.
