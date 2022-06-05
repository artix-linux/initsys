# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=xdm-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for xdm (The original Xorg XDM)"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('xorg-xdm' 'dinit')
provides=('init-xdm' 'init-displaymanager')
conflicts=('init-xdm' 'init-displaymanager')
source=("xdm")
sha256sums=('b70ea544dbca1a711a623dd9c48bd565f3acd7669fe9453b6e60c8f605b50259')

package() {
    install -Dm644 xdm "$pkgdir/etc/dinit.d/xdm"
}
