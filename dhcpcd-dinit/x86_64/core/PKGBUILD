# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=dhcpcd-dinit
pkgver=20230205
pkgrel=1
pkgdesc="dinit service scripts for dhcpcd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-system')
depends=('dhcpcd' 'dinit')
provides=('init-dhcpcd')
conflicts=('init-dhcpcd')
source=("dhcpcd")
sha256sums=('d3ba6f74498f1a92ddbd382260a1f88794210d3ffd9a331e21681b53087f7158')

package() {
    install -Dm644 dhcpcd "$pkgdir/etc/dinit.d/dhcpcd"
}
