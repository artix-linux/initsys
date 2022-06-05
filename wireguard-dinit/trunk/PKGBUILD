# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=wireguard-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service script for wireguard"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('wireguard-tools' 'dinit')
groups=('dinit-world')
conflicts=('init-wireguard')
provides=('init-wireguard')
backup=('etc/dinit.d/config/wireguard.conf')
source=("wireguard"
        "wireguard.script"
        "wireguard.conf")
sha256sums=('5e6f64110f26f7fb6516a8eb7d57beb3ceb0fa9f2f7700974f06babf52da21a6'
            '744d2615bb4923d3880e70c0755f5b459ad457e6ae2a6add3d0d4231c0d08d30'
            'cfc6ca94ab625407cd059e52f48c24691df60b4ee3ae30fd0d0ad0290a57e75e')

package() {
    install -Dm644 wireguard        "$pkgdir/etc/dinit.d/wireguard"
    install -Dm644 wireguard.conf   "$pkgdir/etc/dinit.d/config/wireguard.conf"
    install -Dm755 wireguard.script "$pkgdir/etc/dinit.d/scripts/wireguard"
}
