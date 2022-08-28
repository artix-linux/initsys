# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=dhcp-dinit
pkgver=20211030
pkgrel=3
pkgdesc="dinit service scripts for dhcp"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('dinit' 'dhcp')
provides=('init-dhcp')
conflicts=('init-dhcp')
source=("dhclient"
        "dhcpd4"
        "dhcpd6"
        "dhcpd.script")
sha256sums=('dcf434609fb92e055f72177488602594ae022ce6075abfe5a11799a728720403'
            'efb4791935385dd4390c409a5494f9221ebb1d3d01df445d1900ec66938dceaa'
            '9946e34d945bd0391458a0ac74950f110878befe507ae9fb7655e4d7859761ae'
            '409d1bf595debc5da9433a957c67dfba3bd0e88f7f5ce0112bde8c2abb36591b')

package() {
    install -Dm644 dhclient     "$pkgdir/etc/dinit.d/dhclient"
    install -Dm644 dhcpd4       "$pkgdir/etc/dinit.d/dhcpd4"
    install -Dm644 dhcpd6       "$pkgdir/etc/dinit.d/dhcpd6"
    install -Dm755 dhcpd.script "$pkgdir/etc/dinit.d/scripts/dhcpd"
}
