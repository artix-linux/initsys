# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=znc-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for znc"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('znc' 'dinit')
conflicts=('init-znc')
provides=('init-znc')
source=("znc")
sha256sums=('0d206947d44850a37bc1fc1c984041be6d080d3cfd02fa2f1684225328371946')

package() {
    install -Dm644 znc "$pkgdir/etc/dinit.d/znc"
}
