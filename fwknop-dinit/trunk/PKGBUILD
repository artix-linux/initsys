# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=fwknop-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for fwknop"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('fwknop' 'dinit')
conflicts=('init-fwknop')
provides=('init-fwknop')
source=("fwknopd")
sha256sums=('1e7633310503edf5d086947ca03aafd0c6ead7c727284c6656fc2c1c84712c1a')

package() {
    install -Dm644 fwknopd "$pkgdir/etc/dinit.d/fwknopd"
}
