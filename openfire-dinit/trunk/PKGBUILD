# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=openfire-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for openfire"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('openfire' 'dinit')
conflicts=('init-openfire')
provides=('init-openfire')
source=("openfire")
sha256sums=('328a952ba3d91c2d8e64302229485793074d36ff09725ed386804b95b084ab73')

package() {
    install -Dm644 openfire "$pkgdir/etc/dinit.d/openfire"
}
