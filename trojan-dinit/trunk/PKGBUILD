# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=trojan-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for trojan"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('trojan' 'dinit')
conflicts=('init-trojan')
provides=('init-trojan')
source=("trojan")
sha256sums=('6776c697538927f7724295346b490006784184fe771fd3519cc1f832466ca40f')

package() {
    install -Dm644 trojan "$pkgdir/etc/dinit.d/trojan"
}
