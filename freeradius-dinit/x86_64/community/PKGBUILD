# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=freeradius-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for freeradius"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('freeradius' 'dinit')
conflicts=('init-freeradius')
provides=('init-freeradius')
source=("radiusd")
sha256sums=('6e0fdb4528e736a75224d5e01509aeb89cfbe5208774423e9f9f852e2aee38a8')

package() {
    install -Dm644 radiusd "$pkgdir/etc/dinit.d/radiusd"
}
