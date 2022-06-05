# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=syncthing-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for syncthing"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('syncthing' 'dinit')
conflicts=('init-syncthing')
provides=('init-syncthing')
backup=('etc/dinit.d/config/syncthing.conf' 'etc/dinit.d/syncthing')
source=("syncthing" "syncthing.conf" "syncthing.script")
sha256sums=('cc310ba31990009856120d1df1f89c0b356ee04f41c1b39846a5505e1688f30f'
            '3338d29f61889e77b978cbce35b122346b35fcaf0c675b3602f562d8967330ec'
            'e3f8b9514ffab3a29730f5c0bd93b07b5535581713ef546b53295fd42d857544')

package() {
    install -Dm644 syncthing        "$pkgdir/etc/dinit.d/syncthing"
    install -Dm644 syncthing.conf   "$pkgdir/etc/dinit.d/config/syncthing.conf"
    install -Dm755 syncthing.script "$pkgdir/etc/dinit.d/scripts/syncthing"
}
