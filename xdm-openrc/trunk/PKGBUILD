# Maintainer: artoo <artoo@artixlinux.org>

pkgname=xdm-openrc
pkgver=20220104
pkgrel=1
pkgdesc="OpenRC xdm init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-xdm')
depends=('xorg-xdm' 'openrc')
conflicts=('init-xdm')
source=("xdm.initd")
sha256sums=('d0ec3cf9ca3a010e3ef6e36b66c98bbb1102d9f203a595b642c554952f71d467')

package() {
    install -Dm755 "$srcdir/xdm.initd" "$pkgdir/etc/init.d/xdm"
}
