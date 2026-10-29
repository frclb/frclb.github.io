# frclb.github.io

Alan adının kökü. Burada yalnızca üç şey var:

- `app-ads.txt`: AdMob, yayıncı doğrulamasını mağaza sayfasındaki geliştirici
  sitesinin **kök** adresinde arıyor (`frclb.github.io/app-ads.txt`). Nilu'nun
  sitesi `frclb.github.io/nilu` altında olduğu için dosyanın bir kopyası
  burada duruyor. Kaynağı `frclb/nilu` → `tool/build_site.dart`.
- `index.html`: kök adresi Nilu'nun sitesine yönlendiriyor.
- `.well-known/apple-app-site-association`: Apple, Universal Link
  doğrulamasını alan adının kökünde arıyor. Nilu'nun partner davet bağlantısı
  (`frclb.github.io/nilu/p/#KOD`) bu dosya sayesinde uygulamayı doğrudan
  açıyor. Uygulamadaki karşılığı `frclb/nilu` → `ios/Runner/Runner.entitlements`
  (`applinks:frclb.github.io`). `.nojekyll` olmadan GitHub Pages noktalı
  klasörü yayımlamaz.
