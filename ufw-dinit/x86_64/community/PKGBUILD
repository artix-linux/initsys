# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=ufw-dinit
pkgver=20211103
pkgrel=1
pkgdesc="dinit service scripts for ufw"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('ufw' 'dinit')
conflicts=('init-ufw')
provides=('init-ufw')
source=("ufw")
sha256sums=('571ab6d68609d85e4b226682e4fcfe4b1345d9762d1ae5020412b68415473e6d')

package() {
    install -Dm644 ufw "$pkgdir/etc/dinit.d/ufw"
}
