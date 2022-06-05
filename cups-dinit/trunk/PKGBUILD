# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=cups-dinit
pkgver=20211025
pkgrel=1
pkgdesc="dinit service scripts for cups"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('cups' 'dbus-dinit')
conflicts=('init-cups')
provides=('init-cups')
source=("cupsd")
sha256sums=('ce2e118c4d3449cc4dc03ef4511351b3cbe344c274c85cd94fd26b0cb65d44e2')

package() {
    install -Dm644 cupsd "$pkgdir/etc/dinit.d/cupsd"
}
