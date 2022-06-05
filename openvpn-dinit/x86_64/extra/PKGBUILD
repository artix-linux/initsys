# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=openvpn-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for openvpn"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('openvpn')
source=("openvpn")
sha256sums=('e246a8b6e5b7fc5e8d7d621fa1507fc87e73167f132c320eff1d7a60e6956003')

package() {
    install -Dm644 openvpn "$pkgdir/etc/dinit.d/openvpn"
}
