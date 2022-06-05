# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=postgrey-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for postgrey"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('postgrey' 'dinit')
conflicts=('init-postgrey')
provides=('init-postgrey')
source=("postgrey")
sha256sums=('3f184c1d6eeb562392d3201133c459feed0bb19c6c4440361961428bb1f68d4f')

package() {
    install -Dm644 postgrey "$pkgdir/etc/dinit.d/postgrey"
}
