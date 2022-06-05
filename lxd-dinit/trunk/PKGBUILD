# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=lxd-dinit
pkgver=20211121
pkgrel=2
pkgdesc="dinit service scripts for lxd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('lxd' 'dinit')
conflicts=('init-lxd')
provides=('init-lxd')
source=("lxd" "lxd.script")
sha256sums=('424e40a9c5b69612ef4833c6ab77ae920efffd66b69cb60e3fed7917158e0634'
            '05121a9a1c7d066a4f95a087c6791a6eafe48a624517f6de37fc0e3f81c7dbd7')

package() {
    install -Dm644 lxd        "$pkgdir/etc/dinit.d/lxd"
    install -Dm755 lxd.script "$pkgdir/etc/dinit.d/scripts/lxd"
}
