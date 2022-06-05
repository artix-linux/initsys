# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=tlp-dinit
pkgver=20211103
pkgrel=1
pkgdesc="dinit service scripts for tlp"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('tlp' 'dinit')
conflicts=('init-tlp')
provides=('init-tlp')
source=("tlp")
sha256sums=('bc666b5ce093d0e59e2d33a6d3272e5cc6cf97487e16d6c4e2677bfe32278ea4')

package() {
    install -Dm644 tlp "$pkgdir/etc/dinit.d/tlp"
}
