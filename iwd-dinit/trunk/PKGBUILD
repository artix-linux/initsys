# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=iwd-dinit
pkgver=20211101
pkgrel=1
pkgdesc="dinit service scripts for iwd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('iwd' 'dinit')
conflicts=('init-iwd')
provides=('init-iwd')
source=("iwd")
sha256sums=('90d76ff4764ed43680777f3a848f19096d2ab4063123d8be091cd161a7638069')

package() {
    install -Dm644 iwd "$pkgdir/etc/dinit.d/iwd"
}
