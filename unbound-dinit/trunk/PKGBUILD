# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=unbound-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for unbound"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('unbound' 'dinit')
conflicts=('init-unbound')
provides=('init-unbound')
source=("unbound")
sha256sums=('31bedafb86acb2be1505b7efe4d4140615d22b6576e6ba38c59eac3c2b696c33')

package() {
    install -Dm644 unbound "$pkgdir/etc/dinit.d/unbound"
}
