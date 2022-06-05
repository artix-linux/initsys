# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=xl2tpd-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for xl2tpd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('xl2tpd' 'dinit')
conflicts=('init-xl2tpd')
provides=('init-xl2tpd')
source=("xl2tpd")
sha256sums=('415bde6b8c3adf06d5937780d92fe76a83957a67f7f334596a70785ce457ed17')

package() {
    install -Dm644 xl2tpd "$pkgdir/etc/dinit.d/xl2tpd"
}
