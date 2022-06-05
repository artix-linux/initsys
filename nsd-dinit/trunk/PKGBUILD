# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=nsd-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for nsd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('nsd' 'dinit')
conflicts=('init-nsd')
provides=('init-nsd')
source=("nsd" "nsd.script")
sha256sums=('8ac57e1fbbfbbaad4e9d6cf84571a712fd1a2b6d24cb67f2135a6e9362baede3'
            '330f8c6a5670bee5a1816d5188158c784786c11916478e18a3bef08643fb1aed')

package() {
    install -Dm644 nsd        "$pkgdir/etc/dinit.d/nsd"
    install -Dm755 nsd.script "$pkgdir/etc/dinit.d/scripts/nsd"
}
