# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=haveged-dinit
pkgver=20211026
pkgrel=2
pkgdesc="dinit service scripts for haveged"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('haveged' 'dinit')
conflicts=('init-haveged')
provides=('init-haveged')
source=("haveged")
sha256sums=('e305ffe0361e81ee6163750da8196397c71e1dc9aa25f38a233c96ba5ab0f6a1')

package() {
    install -Dm644 haveged "$pkgdir/etc/dinit.d/haveged"
}
