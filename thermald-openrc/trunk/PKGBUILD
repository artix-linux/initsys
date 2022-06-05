# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=thermald-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC thermald init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('dbus-openrc' 'thermald')
provides=('init-thermald')
conflicts=('init-thermald')
source=("thermald.initd")
sha256sums=('c53e318a6da1e3abd758f864e870f3186ebfe49c729fe65b0f2dd94168e65892')

package() {
    install -Dm 755 "$srcdir/thermald.initd" "$pkgdir/etc/init.d/thermald"
}
