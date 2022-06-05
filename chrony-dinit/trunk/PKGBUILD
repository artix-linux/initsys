# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=chrony-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for chrony"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('chrony' 'dinit')
conflicts=('init-chrony')
provides=('init-chrony')
source=("chronyd")
sha256sums=('43040e2027eb6616497449b9886bfaef83a983edb6cac5d5016c05abb386bec2')

package() {
    install -Dm644 chronyd "$pkgdir/etc/dinit.d/chronyd"
}
