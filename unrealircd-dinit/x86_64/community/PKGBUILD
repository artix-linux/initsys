# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=unrealircd-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for unrealircd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('unrealircd' 'dinit')
conflicts=('init-unrealircd')
provides=('init-unrealircd')
source=("unrealircd")
sha256sums=('aa31e58c54c4153cfce93cb3a4e2745b827b2b1fa80abf31b73a1f51b79c3ef3')

package() {
    install -Dm644 unrealircd "$pkgdir/etc/dinit.d/unrealircd"
}
