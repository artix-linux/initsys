# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=squid-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for squid"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('squid' 'dinit')
conflicts=('init-squid')
provides=('init-squid')
source=("squid")
sha256sums=('9ee633f68d8eb8b55d938ae573866a81621ee7f639155fe1d1c74687cafbe990')

package() {
    install -Dm644 squid "$pkgdir/etc/dinit.d/squid"
}
