# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=bind-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for bind"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('bind' 'dinit')
provides=('init-bind')
conflicts=('init-bind')
source=("named" "named.script")
sha256sums=('9047a4f43d31546755a9ebb6ff1f837498fd023b2c6e689720a8b3706bde9d3a'
            '389964904d120d6401caa4abf77aa5e90b19e35335dc773a29b09bb7440b3014')

package() {
    install -Dm644 named        "$pkgdir/etc/dinit.d/named"
    install -Dm755 named.script "$pkgdir/etc/dinit.d/scripts/named"
}
