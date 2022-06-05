# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=udpxy-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for udpxy"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('udpxy' 'dinit')
conflicts=('init-udpxy')
provides=('init-udpxy')
source=("udpxy")
sha256sums=('9afbfed67b4f033e82782944ac272af7487fcfe2bb605f46b6e3c7019bc25a6b')

package() {
    install -Dm644 udpxy "$pkgdir/etc/dinit.d/udpxy"
}
