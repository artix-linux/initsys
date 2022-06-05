# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=strongswan-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for strongswan"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('strongswan' 'dinit')
conflicts=('init-strongswan')
provides=('init-strongswan')
source=("strongswan")
sha256sums=('2ca945ab6bcb0bf9c56ab4bc4753ed474750b70b2ea6cab6c0cc5b22e0bd781b')

package() {
    install -Dm644 strongswan "$pkgdir/etc/dinit.d/strongswan"
}
