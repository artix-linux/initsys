# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=gpm-dinit
pkgver=20211029
pkgrel=1
pkgdesc="dinit service scripts for gpm"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-system')
depends=('gpm' 'dinit')
conflicts=('init-gpm')
provides=('init-gpm')
source=("gpm")
sha256sums=('7c53331b6d0932687d7b30b8547d77b361edf9c4f51c96e21d2d8b18832c01bd')

package() {
    install -Dm644 gpm "$pkgdir/etc/dinit.d/gpm"
}
