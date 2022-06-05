# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=toxcore-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for toxcore"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('toxcore' 'dinit')
conflicts=('init-toxcore')
provides=('init-toxcore')
source=("toxbootstrapd")
sha256sums=('e0dd75613a1ef1386581ec70c6b12d2ce7f9611c44dbe3decde8d543757aa84a')

package() {
    install -Dm644 toxbootstrapd "$pkgdir/etc/dinit.d/toxbootstrapd"
}
