# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=intel-undervolt-dinit
pkgver=20211101
pkgrel=1
pkgdesc="dinit service scripts for intel-undervolt"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('intel-undervolt' 'dinit')
conflicts=('init-intel-undervolt')
provides=('init-intel-undervolt')
source=("intel-undervolt" "intel-undervolt-loop")
sha256sums=('b270476b8507b69d8f676408bdc3b14344793f976decd0b00c30cec6917e3d3e'
            '6b30ca4c3dca4a6d68b21cc37bace6cb090db2635784e6fdd02893cfee1f2aa9')

package() {
    install -Dm644 intel-undervolt      "$pkgdir/etc/dinit.d/intel-undervolt"
    install -Dm644 intel-undervolt-loop "$pkgdir/etc/dinit.d/intel-undervolt-loop"
}
