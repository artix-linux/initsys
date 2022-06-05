# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=shairport-sync-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for shairport-sync"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('shairport-sync' 'dinit')
conflicts=('init-shairport-sync')
provides=('init-shairport-sync')
source=("shairport-sync")
sha256sums=('cfccc2684a848ab3e0f3e47136123be2f5e7f759d0cf3d26be462733f764750e')

package() {
    install -Dm644 shairport-sync "$pkgdir/etc/dinit.d/shairport-sync"
}
