# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=apache-dinit
pkgver=20211025
pkgrel=2
pkgdesc="dinit service scripts for apache"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('apache' 'dinit')
conflicts=('init-apache')
provides=('init-apache')
source=("apache")
sha256sums=('605c30d7cff5596808ba11a3f58394c752fee0862289aeeed17947a0c3ca584f')

package() {
    install -Dm644 apache "$pkgdir/etc/dinit.d/apache"
}
