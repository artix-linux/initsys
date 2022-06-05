# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=espeakup-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for espeakup"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('espeakup' 'dinit')
conflicts=('init-espeakup')
provides=('init-espeakup')
source=("espeakup" "espeakup.script")
sha256sums=('b1e64927867f7e8433625daa11564e943095dc8ad3ce9a1015099e8e56befc37'
            '2d381a03baa4fde70008fe9756bf075de377ae5b53658ddeb1f43492253cdcda')

package() {
    install -Dm644 espeakup        "$pkgdir/etc/dinit.d/espeakup"
    install -Dm755 espeakup.script "$pkgdir/etc/dinit.d/scripts/espeakup"
}
