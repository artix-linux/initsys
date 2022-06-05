# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=bolt-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for bolt"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('bolt' 'dinit')
conflicts=('init-bolt')
provides=('init-bolt')
source=("boltd")
sha256sums=('dabd3d9991042c6e99436c1124584f728cface64e84f5b626c7ebe7bb8cdcc11')

package() {
    install -Dm644 boltd "$pkgdir/etc/dinit.d/boltd"
}
