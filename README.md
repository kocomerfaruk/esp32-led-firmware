# esp32-led-firmware

ESP32 LED projesinin imzalı OTA yazılım dosyaları. Dosyalar GitHub Pages üzerinden HTTPS ile sunulur.

- `latest.json`: son sürümün adresi, boyutu, SHA-256 özeti ve ECDSA P-256 imzası
- `fw/<sha256>.bin`: yazılım dosyaları (son birkaç sürüm)

Cihaz bir dosyayı yalnızca imzası, cihazdaki açık anahtarla doğrulanırsa kurar. Yeni yazılım sağlıklı açılmazsa
cihaz otomatik olarak önceki sürüme döner. Yazılım dosyaları şifre içermez; cihaza özel bilgiler cihazın kendi
hafızasında tutulur.

Bu depo yayın betiği tarafından her seferinde geçmişsiz tek bir commit ile güncellenir.
