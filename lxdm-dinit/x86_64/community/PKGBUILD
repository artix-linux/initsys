# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=lxdm-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for lxdm"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('lxdm' 'dinit')
conflicts=('init-lxdm')
provides=('init-lxdm')
source=("lxdm")
sha256sums=('0545a98fbaabdb0883bcf8c15a37368a8952eee68d440ebfd92f817ceef9f36a')

package() {
    install -Dm644 lxdm "$pkgdir/etc/dinit.d/lxdm"
}
