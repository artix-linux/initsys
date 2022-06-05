# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=rpcbind-dinit
pkgver=20211029
pkgrel=3
pkgdesc="dinit service scripts for rpcbind"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-system')
depends=('rpcbind' 'dinit')
provides=('init-rpcbind')
conflicts=('init-rpcbind')
source=("rpcbind")
sha256sums=('0eeb8740274fe8af77894cb0566949d9d76bdf041b9352fe7407a0c24d38a835')

package() {
    install -Dm644 rpcbind "$pkgdir/etc/dinit.d/rpcbind"
}
