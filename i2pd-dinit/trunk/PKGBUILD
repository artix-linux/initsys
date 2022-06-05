# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=i2pd-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for i2pd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('i2pd' 'dinit')
conflicts=('init-i2pd')
provides=('init-i2pd')
source=("i2pd")
sha256sums=('37801f82bf13eb5953fb1266b5b744e959a09cf372870b93108c5172659207bd')

package() {
    install -Dm644 i2pd "$pkgdir/etc/dinit.d/i2pd"
}
