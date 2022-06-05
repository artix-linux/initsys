# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=knot-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for knot"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('knot' 'dinit')
conflicts=('init-knot')
provides=('init-knot')
source=("knotd")
sha256sums=('b6d09bdc9241b0db33499d55be5a6c2a86b5fcebc279ee8d50551ee588d106af')

package() {
    install -Dm644 knotd "$pkgdir/etc/dinit.d/knotd"
}
