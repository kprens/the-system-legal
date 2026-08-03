# THE SYSTEM — hukuki ve destek sayfaları

App Store Connect ve Google Play, gizlilik politikası ve destek için herkese
açık bir URL istiyor. Bu depo yalnız o sayfaları barındırır. **Uygulama kodu
burada değildir.**

| Sayfa | Adres |
|---|---|
| Gizlilik Politikası | `privacy.html` |
| Kullanım Koşulları | `terms.html` |
| Destek | `support.html` |
| Dizin | `index.html` |

## ELLE DÜZENLEME

Bu HTML dosyaları **üretilmiştir**. Kaynakları uygulamanın kendi metinleridir:

- `src/lib/privacyText.ts`
- `src/lib/termsText.ts`

Üreten betik: `scripts/build-legal.mjs` (ana depoda).

Buradaki bir dosyayı elle değiştirirsen, **mağazadaki metin ile uygulamanın
içindeki metin ayrışır**. Bu yalnızca özensizlik değil, bir uyum sorunudur:
kullanıcı uygulamada bir şey okur, mağazada başka bir şey okur.

Değişiklik gerekiyorsa ana depodaki metin dosyasını düzenle, `npm run legal`
çalıştır ve üretilen dosyaları buraya kopyala. Ana depodaki `npm test`,
sayfaların uygulamayla aynı olduğunu her çalıştırmada doğruluyor.

## Yayın

GitHub Pages: Settings → Pages → Deploy from a branch → `main` / `(root)`.
