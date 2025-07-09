# Maintainer: Philip J. Repko <philipjrepko@gmail.com>
pkgname=sqlch-suite
pkgver=2.0.0
pkgrel=1
pkgdesc="Terminal-based internet radio suite with TUI, tray, and controller"
arch=('any')
url="https://github.com/SW-philip/sqlch-suite"
license=('MIT')
depends=('bash' 'mpv' 'gtk3' 'python' 'python-gobject' 'libayatana-appindicator' 'hicolor-icon-theme')
optdepends=(
  'gum: TUI interface in sqlchknob'
  'jq: JSON parsing for radio-browser search'
)
source=("${pkgname}-${pkgver}.tar.gz::https://codeload.github.com/SW-philip/${pkgname}/tar.gz/refs/tags/v${pkgver}")
sha256sums=('458cff80239f117b5aa2c50989bda9d4744f5a70491bd074338ab1224e6852b2')

package() {
  cd "$srcdir/${pkgname}-${pkgver}"

  install -Dm755 sqlchctl "$pkgdir/usr/bin/sqlchctl"
  install -Dm755 sqlchknob "$pkgdir/usr/bin/sqlchknob"
  install -Dm755 sqlchtray "$pkgdir/usr/bin/sqlchtray"

  install -Dm644 sqrlch_icon.png "$pkgdir/usr/share/icons/hicolor/512x512/apps/sqlch.png"
  install -Dm644 stations.default "$pkgdir/etc/skel/.config/sqlch/stations"
  install -Dm644 channels.default "$pkgdir/etc/skel/.config/sqlch/channels"
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
