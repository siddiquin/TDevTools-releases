# TDevTools

**Geliştiriciler için ücretsiz bir masaüstü araç takımı: macOS, Windows ve Linux'ta JSON, XML, şemalar, API'ler, kodlama ve sertifikalar için 47 araç.**

[transposal.app](https://transposal.app) tarafından

**Dili seçin:** [English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Türkçe](README.tr.md) · [日本語](README.ja.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md)

> **🔒 Yerel olarak çalışır. Verileriniz bilgisayarınızdan çıkmaz.** TDevTools tüm işlemleri kendi bilgisayarınızda yapar. JSON ve XML dosyalarınız, belirteçleriniz, anahtarlarınız ve sertifikalarınız yüklenmez veya analiz hizmetlerine gönderilmez. Hesap ya da izleme yoktur. Uygulama internete yalnızca siz istediğinizde bağlanır: URL yüklerken, API'nize test isteği gönderirken veya bir sunucunun sertifikasını alırken. Diğer tüm araçlar çevrimdışı çalışır.

## Ekran görüntüleri

**JSON → JSON Schema:** örnek verilerden şema çıkarın.

![JSON'dan JSON Schema'ya](screenshots/json-to-schema.png)

**API Test Aracı:** istek gönderin; yanıtları ağaç, tablo veya metin olarak inceleyin.

![API Test Aracı](screenshots/api-tester.png)

**Sertifika İnceleyici:** sertifika zincirini görüntüleyin, sertifikaları ve imzaları denetleyin.

![Sertifika İnceleyici](screenshots/certificate-inspector.png)

## İndirme

En son sürümü [Sürümler sayfasından](https://github.com/siddiquin/TDevTools-releases/releases/latest) indirin.

| Sistem | İndirilecek dosya |
| --- | --- |
| macOS, Apple Silicon (M1–M4) | `TDevTools-<version>-arm64.dmg` |
| macOS, Intel | `TDevTools-<version>-x64.dmg` |
| Windows 10/11, 64 bit | `TDevTools-Setup-<version>-x64.exe` |
| Windows 10/11, ARM | `TDevTools-Setup-<version>-arm64.exe` |
| Windows, taşınabilir | `TDevTools-Portable-<version>.exe` |
| Linux, 64 bit (x86_64) | `TDevTools-<version>-x86_64.AppImage` |
| Linux, ARM64 | `TDevTools-<version>-arm64.AppImage` |

**Sistem gereksinimleri:** macOS 12 Monterey veya üzeri; Windows 10/11 (64 bit veya ARM64); ya da güncel bir 64 bit Linux dağıtımı (Ubuntu 20.04+, Debian 11+, Fedora 36+ veya benzeri). Yaklaşık 300 MB boş disk alanı gerekir.

## Kurulum

### macOS

1. Mac'inize uygun `.dmg` dosyasını indirin, açın ve lisans sözleşmesini kabul edin.
2. **TDevTools**'u **Uygulamalar** klasörüne sürükleyin ve disk görüntüsünü çıkarın.
3. İlk açılışta macOS, ücretli Apple Developer sertifikasıyla imzalanmadığı için uygulamanın doğrulanamadığını bildirebilir. Bu beklenen bir durumdur; uygulamayı yalnızca bir kez onaylamanız gerekir.
   - **macOS 14 ve öncesi:** Finder'da TDevTools'a sağ tıklayın, **Aç**'ı seçin ve tekrar onaylayın.
   - **macOS 15 ve sonrası:** Uygulamayı açmayı deneyin ve uyarıda **Bitti**'ye tıklayın. **Sistem Ayarları → Gizlilik ve Güvenlik** bölümüne gidip TDevTools engelleme uyarısının yanındaki **Yine de Aç**'ı seçin ve onaylayın.
4. macOS «TDevTools has been damaged» derse önce dosyanın resmi [Sürümler sayfasından](https://github.com/siddiquin/TDevTools-releases/releases/latest) indirildiğini doğrulayın. Ardından Terminal'de `xattr -dr com.apple.quarantine /Applications/TDevTools.app` komutunu çalıştırarak yalnızca bu uygulamanın indirme işaretini kaldırın.

### Windows

- **Yükleyici:** `TDevTools-Setup-<version>-x64.exe` dosyasını (ARM bilgisayarlar için `arm64`) çalıştırın, lisansı kabul edin ve **Yükle**'yi seçin. SmartScreen «Windows bilgisayarınızı korudu» derse **Daha fazla bilgi → Yine de çalıştır**'ı seçin. Yükleme yalnızca kullanıcı hesabınız içindir; yönetici izni gerekmez.
- **Taşınabilir sürüm:** `TDevTools-Portable-<version>.exe` dosyasını çalıştırın. SmartScreen uyarısında **Daha fazla bilgi → Yine de çalıştır**'ı seçin.

### Linux (AppImage)

Uygun dosyayı indirin; **Özellikler → İzinler** bölümünden veya `chmod +x TDevTools-*.AppImage` komutuyla çalıştırma izni verin. Dosyayı çift tıklayarak ya da Terminal'den çalıştırın. Başlamazsa bazı dağıtımlarda FUSE 2 gerekir (Ubuntu/Debian: `sudo apt install libfuse2`; Ubuntu 24.04: `sudo apt install libfuse2t64`; Fedora: `sudo dnf install fuse-libs`). Uygulama menüsüne eklemek için Gear Lever veya AppImageLauncher kullanabilirsiniz.

## Güncelleme ve kaldırma

Yeni sürümü indirip aynı şekilde yükleyin; tercihleriniz korunur. macOS'ta Uygulamalar'daki uygulamayı değiştirin, Windows'ta yeni yükleyiciyi çalıştırın, Linux'ta AppImage dosyasını yenisiyle değiştirin.

- **macOS:** TDevTools'u Çöp Sepeti'ne taşıyın. Tercihleri de silmek için `~/Library/Application Support/TDevTools` klasörünü silin.
- **Windows:** **Ayarlar → Uygulamalar → Yüklü uygulamalar** bölümünden TDevTools'u kaldırın. Tercihler için `%APPDATA%\TDevTools` klasörünü silin. Taşınabilir sürümde `.exe` dosyasını silmeniz yeterlidir.
- **Linux:** AppImage dosyasını silin. Tercihler için `~/.config/TDevTools` klasörünü silin.

Uygulama yalnızca tema ve dil gibi tercihlerinizi saklar; verilerinizin, parolalarınızın veya anahtarlarınızın kopyalarını tutmaz.

## Özellikler

- **Biçimlendirme ve doğrulama:** JSON biçimlendirici, doğrulayıcı, onarıcı ve görsel düzenleyici; JSON, XML, CSV, Excel, YAML, TOON ve JSONL dönüşümleri; Markdown, JSON/XML şemaları (XSD) ve TypeScript türleri.
- **Güvenlik:** JWT çözümleme, doğrulama ve imzalama; Base64/URL/SAML kodlama; MD5, SHA-1 ve SHA-256 özetleri; kendinden imzalı sertifika ve mTLS kiti oluşturma; sertifika, açık anahtar ve JKS deposu inceleme.
- **Görüntüleme ve API:** ağaç, tablo, ızgara, grafik ve ham JSON görünümleri; OpenAPI/Swagger gezgini, OAuth2 ve mTLS destekli HTTP istemcisi, SOAP/WSDL görüntüleyici, dosya görüntüleyici ve Markdown önizlemesi.
- **Sorgu ve dönüştürme:** JSONPath test aracı, düzenli ifadeli arama ve değiştirme, JavaScript/TypeScript/Python/C# olarak dışa aktarılabilen JSON eşleyici; isteğe bağlı bulut hizmeti Transposal Mapper.
- **Karşılaştırma:** JSON/XML yapısal farkları ve satır düzeyinde hatalarla JSON Schema doğrulaması.
- **Uygulamanın tamamında:** 8 dil, 6 tema, vurgu renkleri, yoğunluk ve yakınlaştırma, tek tıkla kopyalama, sağ tık menüsü, sürükle-bırak ve durum çubuğunda CPU/bellek kullanımı.

## Gizlilik ve güvenlik

- Tüm işlemler bilgisayarınızda yapılır; yapıştırdığınız veya açtığınız hiçbir şey yüklenmez.
- Hesap, telemetri ve reklam yoktur.
- Ağ bağlantısı yalnızca URL yüklemek, API'yi test etmek veya sertifika almak gibi sizin başlattığınız işlemlerde kurulur.
- Parolalar, belirteçler ve özel anahtarlar yalnızca uygulama açıkken bellekte tutulur; sadece tercihler kaydedilir.
- Yalıtılmış pencereler ve katı içerik güvenlik ilkesi kullanılır; HTML önizlemeleri betik çalıştırmaz; program veya betik açmadan önce onay istenir; oturum açma bilgileri yalnızca seçtiğiniz sunucuya gönderilir.
- Yerleşik örnekler herkese açık demo sunucularını kullanır ve 2 dakikada bir istekle sınırlandırılır. Kendi URL ve dosyalarınız sınırsızdır.

## Sık sorulan sorular

**TDevTools ücretsiz mi?** Evet, geliştiriciler için ücretsizdir. [Lisans Sözleşmesi'ne](LICENSE.md) bakın.

**Çevrimdışı çalışır mı?** Evet; yalnızca seçtiğiniz sunucuyla iletişim kurması gereken özellikler (URL yükleme, API/SOAP testi, sertifika zinciri alma) çevrimdışı çalışmaz.

**Kaynak kodu açık mı?** TDevTools kapalı kaynaklıdır. Kaynak kodunu **<support@transposal.app>** adresinden, «TDevTools» konulu e-postayla talep edebilirsiniz.

**Kurulum sırasında bilgisayarım neden uyarı veriyor?** Uygulama ücretli Apple veya Microsoft geliştirici sertifikasıyla imzalanmamıştır; bu nedenle Gatekeeper ve SmartScreen ilk açılışta uyarı gösterir. Kurulum adımlarını izleyin ve yalnızca resmi [Sürümler sayfasından](https://github.com/siddiquin/TDevTools-releases/releases/latest) indirin.

## Lisans ve destek

- [Son Kullanıcı Lisans Sözleşmesi](LICENSE.md): ücretsiz kullanım, garanti verilmez. Sözleşmenin tamamı uygulamada **Yardım → Lisans Sözleşmesi** altında 8 dilde bulunur.
- [Üçüncü taraf bildirimleri](THIRD_PARTY_NOTICES.md)
- Destek: **<support@transposal.app>**
- Web sitesi: [transposal.app](https://transposal.app)

© 2026 Transposal. Tüm hakları saklıdır.