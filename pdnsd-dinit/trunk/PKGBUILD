# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=pdnsd-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for pdnsd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('pdnsd' 'dinit')
conflicts=('init-pdnsd')
provides=('init-pdnsd')
source=("pdnsd")
sha256sums=('3b33c201f1b099869f65e0ef31b7915ef0c381ce556af87f0f00855b96277911')

package() {
    install -Dm644 pdnsd "$pkgdir/etc/dinit.d/pdnsd"
}
