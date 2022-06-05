# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=mdadm-dinit
pkgver=20211029
pkgrel=1
pkgdesc="dinit service scripts for mdadm"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-system')
depends=('mdadm' 'dinit')
provides=('init-mdadm')
conflicts=('init-mdadm')
source=("mdadm")
sha256sums=('2f32d06ff56c443ddfe16ff6ac1103e552ed59ed1093450f8e348fca49e1627e')

package() {
    install -Dm644 mdadm "$pkgdir/etc/dinit.d/mdadm"
}
