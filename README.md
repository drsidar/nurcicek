# Nur Çiçek & Çikolata — Web Sitesi

Adıyaman'da hizmet veren Nur Çiçek & Çikolata için hazırlanmış, yönetim paneli (admin) üzerinden içeriği güncellenebilen web sitesi.

## Klasördeki dosyalar
- `index.html` — Ana sayfa
- `admin/index.html` — Ürün ve ayarları yönetmek için şifreli panel
- `app.js`, `style.css` — Ortak kod ve tasarım
- `netlify/functions/data.mjs` — Verileri bulutta (Netlify Blobs) saklayan sunucu fonksiyonu
- `netlify.toml` — Netlify yapılandırması
- `images/logo.png` — Logo görseli

## Kurulum (GitHub + Netlify)

1. Bu klasörün tamamını bir GitHub deposuna (repository) yükleyin.
2. [Netlify](https://app.netlify.com) hesabınızla "Add new site → Import an existing project" seçip GitHub deponuzu bağlayın.
3. Build ayarları:
   - **Build command:** boş bırakın
   - **Publish directory:** `.`
4. Netlify panelinde **Site configuration → Environment variables** kısmına gidin ve şu değişkeni ekleyin:
   - `ADMIN_PASSWORD` = admin paneline giriş için kullanacağınız gizli şifre
5. Deploy edin. Site birkaç saniye içinde yayında olacak.
6. `siteniz.netlify.app/admin/` adresinden panele girip ürünleri ve site ayarlarını (telefon, adres, Google/Yandex link vb.) düzenleyebilirsiniz.

> Not: `ADMIN_PASSWORD` ortam değişkenini eklemezseniz kaydetme (Buluta Kaydet) işlemi çalışmaz — bu kasıtlı bir güvenlik önlemidir.
