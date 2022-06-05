# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=ddclient-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for ddclient"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('ddclient' 'dinit')
conflicts=('init-ddclient')
provides=('init-ddclient')
source=("ddclient")
sha256sums=('0b01e247c2e696f1c252ea820dd9cd157da96aac4404aa290cae0b1b3efd4d16')

package() {
    install -Dm644 ddclient "$pkgdir/etc/dinit.d/ddclient"
}
