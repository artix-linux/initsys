# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=motion-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for motion"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('motion' 'dinit')
conflicts=('init-motion')
provides=('init-motion')
source=("motion")
sha256sums=('fdd4ecc6792248221988bce20be05664a12e8f20a2e6b5a93bb8552ae028c677')

package() {
    install -Dm644 motion "$pkgdir/etc/dinit.d/motion"
}
