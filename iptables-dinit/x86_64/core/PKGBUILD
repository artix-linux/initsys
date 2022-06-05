# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=iptables-dinit
pkgver=20211029
pkgrel=4
pkgdesc="dinit service scripts for iptables"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-system')
depends=('iptables' 'dinit')
provides=('init-iptables')
conflicts=('init-iptables')
source=("iptables"
        "ip6tables")
sha256sums=('5b5864d3c2d5d41bdf5c43daa640087aeae9c1ff02c9503581fb5fe01d27502b'
            'f5b2d3aed65afceeadfaadc6c669e36593aac957b8f9d7034a86ddb0c28e42b2')

package() {
    install -Dm644 iptables  "$pkgdir/etc/dinit.d/iptables"
    install -Dm644 ip6tables "$pkgdir/etc/dinit.d/ip6tables"
}
