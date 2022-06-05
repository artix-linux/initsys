# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=lighttpd-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for lighttpd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('dinit' 'lighttpd')
provides=('init-lighttpd')
conflicts=('init-lighttpd')
source=("lighttpd")
sha256sums=('b5b3e4dd79cbcdf8e9964b8f708b1a5cb9814444f6756d5d6f0ad54c341e0fb8')

package() {
    install -Dm644 lighttpd "$pkgdir/etc/dinit.d/lighttpd"
}
