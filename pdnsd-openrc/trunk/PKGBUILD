# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=pdnsd-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC pdnsd init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'pdnsd')
provides=('init-pdnsd')
conflicts=('init-pdnsd')
source=("pdnsd.initd")
sha256sums=('8ae0dc4373fe99e3880b9b9b9b32e4853b04d8bb47eff759626db56b19dac8e0')

package() {
    install -Dm755 "$srcdir/pdnsd.initd" "$pkgdir/etc/init.d/pdnsd"
}
