# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=tor-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for tor"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('tor' 'dinit')
conflicts=('init-tor')
provides=('init-tor')
source=("tor")
sha256sums=('daaed205e3bf4242ce969b0c90132fb138c17352e2b7d5ca444d3d61aafccbd2')

package() {
    install -Dm644 tor "$pkgdir/etc/dinit.d/tor"
}
