# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=sslh-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for sslh"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('sslh' 'dinit')
conflicts=('init-sslh')
provides=('init-sslh')
source=("sslh")
sha256sums=('401056cd3338d292d301e78e3abe4d26602c570aabe03e81ac2fd67e57ed63ac')

package() {
    install -Dm644 sslh "$pkgdir/etc/dinit.d/sslh"
}
