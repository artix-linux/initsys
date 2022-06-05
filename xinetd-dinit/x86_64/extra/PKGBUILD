# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=xinetd-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for xinetd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('xinetd' 'dinit')
provides=('init-xinetd')
conflicts=('init-xinetd')
source=("xinetd")
sha256sums=('1dc3d1343bef13f6c7ce7680d0c4b9e65dd59ba42ac80ca24a602059e23b8964')

package() {
    install -Dm644 xinetd "$pkgdir/etc/dinit.d/xinetd"
}
