# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=minidlna-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for minidlna"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('minidlna' 'dinit')
conflicts=('init-minidlna')
provides=('init-minidlna')
source=("minidlnad")
sha256sums=('6d3ad3b2ed3ed2f324074a7539298c62c3d4a1ee2f959bd9c516b1312f55753b')

package() {
    install -Dm644 minidlnad "$pkgdir/etc/dinit.d/minidlnad"
}
