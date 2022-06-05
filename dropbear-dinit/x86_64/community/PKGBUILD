# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=dropbear-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for dropbear"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('dropbear' 'dinit')
conflicts=('init-dropbear')
provides=('init-dropbear')
source=("dropbear")
sha256sums=('fee073e8688673d27f8cdaede53b97dc30e3d76bc34fc67418f16c05f585a1f7')

package() {
    install -Dm644 dropbear "$pkgdir/etc/dinit.d/dropbear"
}
