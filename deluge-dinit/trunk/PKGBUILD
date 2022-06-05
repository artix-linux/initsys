# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=deluge-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for deluge"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('dinit' 'deluge')
provides=('init-deluge')
conflicts=('init-deluge')
source=("deluged"
        "deluge-web")
sha256sums=('41a9b3636ae9690b8c4fdd9463d66b1941f99b26c417f65b77cb7ac263f632da'
            '7f3ebff2b1e5b73f8aeb0025d10229e2c4769527cb9f5f3075b87fb6983701b2')

package() {
    install -Dm644 deluged    "$pkgdir/etc/dinit.d/deluged"
    install -Dm644 deluge-web "$pkgdir/etc/dinit.d/deluge-web"
}
