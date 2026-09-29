# Teker Fırlat — Yayın web sitesi

App Store Connect'in istediği URL'ler için statik site (derleme gerektirmez).

| Dosya | App Store Connect alanı |
|---|---|
| `privacy.html` | **Privacy Policy URL** (zorunlu) |
| `support.html` | **Support URL** (zorunlu) |
| `index.html` | Marketing URL (isteğe bağlı) |
| `terms.html` | Kullanım koşulları (isteğe bağlı; Apple standart EULA'ya bağlanır) |
| `app-ads.txt` | AdMob doğrulaması — **alan adının kökünde** olmalı |

## Yayımlamadan önce doldurulacaklar

Sarı vurgulu (`class="todo"`) yerleri arayın:

- `destek@ORNEK-ALAN-ADI.com` → gerçek destek e-postanız (tüm sayfalarda)
- `[Geliştirici adı / şirket unvanı, adres]` → privacy.html (TR + EN)
- Yürürlük tarihleri
- `app-ads.txt` → `pub-XXXXXXXXXXXXXXXX` AdMob yayıncı kimliğiniz
- `index.html` → App Store bağlantısı ve `apple-itunes-app` meta etiketi (yayından sonra)
- Oyundaki bağlantılar: `src/config.js` → `APP_INFO.privacyUrl / supportUrl`

## GitHub Pages ile yayımlama (ücretsiz)

1. GitHub'da yeni bir depo açın (örn. `teker-firlat`).
2. Bu klasörün içeriğini deponun köküne (veya `docs/` klasörüne) koyup push edin.
3. Settings → Pages → Branch: `main`, klasör: `/ (root)` veya `/docs`.
4. Adres: `https://KULLANICI.github.io/teker-firlat/`

> **app-ads.txt uyarısı:** AdMob, dosyayı alan adının kökünde arar
> (`https://KULLANICI.github.io/app-ads.txt`). Proje sayfasında (`/teker-firlat/`) yayımlarsanız
> bulunmaz. Çözüm: `KULLANICI.github.io` adlı ayrı bir depoya yalnızca `app-ads.txt` koyun
> **veya** kendi alan adınızı bağlayın (önerilir). Netlify / Cloudflare Pages ile özel alan adında
> dosya zaten kökte olur.

## Netlify / Cloudflare Pages

Bu klasörü sürükle-bırak ile yükleyin; derleme komutu yok, yayın klasörü `website/`.
