# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=coturn-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for coturn"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('coturn' 'dinit')
conflicts=('init-coturn')
provides=('init-coturn')
source=("coturn")
sha256sums=('aab28daeafa153eecc1f5594d91b90bc6885d4881d73b4996915a846ab0740e7')

package() {
    install -Dm644 coturn "$pkgdir/etc/dinit.d/coturn"
}
