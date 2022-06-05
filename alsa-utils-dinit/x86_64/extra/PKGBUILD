# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=alsa-utils-dinit
pkgver=20211025
pkgrel=2
pkgdesc="dinit service scripts for alsa-utils"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('alsa-utils' 'dinit')
provides=('init-alsa-utils')
conflicts=('init-alsa-utils')
install=alsa-utils-dinit.install
source=("alsa")
sha256sums=('e6d037fb50cd1333185921651faf9304c5695465911f9bca8d39638addb87ad8')

package() {
    install -d "$pkgdir/etc/dinit.d"
    install -Dm644 alsa "$pkgdir/etc/dinit.d/alsa"
}
