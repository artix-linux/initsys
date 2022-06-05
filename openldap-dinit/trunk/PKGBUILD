# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=openldap-dinit
pkgver=20211030
pkgrel=1
pkgdesc="dinit service scripts for openldap"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-system')
depends=('openldap' 'dinit')
provides=('init-openldap')
conflicts=('init-openldap')
source=("slapd")
sha256sums=('c19e416586040ae285e9a7399c8223b0ce4f693e6eeb1856e4b31a94f84fb9b3')

package() {
    install -Dm644 slapd "$pkgdir/etc/dinit.d/slapd"
}
