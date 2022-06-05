# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=rsync-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for rsync"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('rsync' 'dinit')
conflicts=('init-rsync')
provides=('init-rsync')
source=("rsync")
sha256sums=('27ee3f868f41add9367dfb280cc5418f7e5c658aca0a659b63a08b25664299c4')

package() {
    install -Dm644 rsync "$pkgdir/etc/dinit.d/rsync"
}
