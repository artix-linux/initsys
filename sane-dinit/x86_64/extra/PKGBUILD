# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=sane-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for sane"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('sane' 'dinit')
conflicts=('init-sane')
provides=('init-sane')
source=("saned")
sha256sums=('b8281bca3f168abce7fe4560d992cc3b977b653a98b4cb0402219cdb46affe7b')

package() {
    install -Dm644 saned "$pkgdir/etc/dinit.d/saned"
}
