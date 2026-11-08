# frclb.github.io

Alan adının kökü. Burada yalnızca üç şey var:

- `app-ads.txt`: AdMob, yayıncı doğrulamasını mağaza sayfasındaki geliştirici
  sitesinin **kök** adresinde arıyor (`frclb.github.io/app-ads.txt`). Nilu'nun
  sitesi `frclb.github.io/nilu` altında olduğu için dosyanın bir kopyası
  burada duruyor. Yayıncı kimliği uygulamanın gizli deposunda
  (`frclb/nilu-app` → `lib/core/release_config.dart`); dosyayı
  `tool/build_site.dart` üretiyor.
- `index.html`: kök adresi Nilu'nun sitesine yönlendiriyor.
- `.well-known/apple-app-site-association`: Apple, Universal Link
  doğrulamasını alan adının kökünde arıyor. Nilu'nun partner davet bağlantısı
  (`frclb.github.io/nilu/p/#KOD`) ve e-posta doğrulama / şifre yenileme
  bağlantısı (`frclb.github.io/nilu/auth/?mode=…`) bu dosya sayesinde
  uygulamayı doğrudan açıyor. Uygulamadaki karşılığı
  `frclb/nilu-app` → `ios/Runner/Runner.entitlements`
  (`applinks:frclb.github.io`). `.nojekyll` olmadan GitHub Pages noktalı
  klasörü yayımlamaz.

## Depolar

- `frclb/nilu` (açık): yalnızca Nilu'nun üretilmiş sitesi; uygulama kodu
  orada yok. Yeniden adlandırılırsa `/nilu/` yolları ve uygulamadaki
  bağlantılar bozulur.
- `frclb/nilu-app` (gizli): uygulamanın kodu. Site oradan
  `tool/publish_site.sh` ile üretilip `frclb/nilu`'ya gönderiliyor.
