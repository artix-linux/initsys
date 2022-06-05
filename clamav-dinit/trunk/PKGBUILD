# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=clamav-dinit
pkgver=20211030
pkgrel=1
pkgdesc="dinit service scripts for clamav"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('clamav' 'dinit')
conflicts=('init-clamav')
provides=('init-clamav')
source=("clamd" "clamd.script" "freshclam")
sha256sums=('5d2f422249fc4ea04240efcadd7fac9cd653591b96b1d5e497079ccbc3381bee'
            'd5a3e199debb287e24b4f6f829559a534b0b3c058b72fe5912acb2dc3f2dd47c'
            '056285ad573a940d6e0c9c07d45cf949a426b512ef9ec5b488af394ef39a3768')

package() {
    install -Dm644 clamd        "$pkgdir/etc/dinit.d/clamd"
    install -Dm755 clamd.script "$pkgdir/etc/dinit.d/scripts/clamd"
    install -Dm644 freshclam    "$pkgdir/etc/dinit.d/freshclam"
}
