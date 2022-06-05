# Maintainer: Nathan Owens <ndowens@artixlinux.org>
# Contributor: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=privoxy-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC privoxy init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'privoxy')
provides=('init-privoxy')
conflicts=('init-privoxy')
source=("privoxy.initd")
sha256sums=('e40431d539b9a1738c77dbeebea7c7b02e6b8e8952d5fa6d2a28415dc8ab7e47')

package() {
    install -Dm755 "$srcdir/privoxy.initd" "$pkgdir/etc/init.d/privoxy"
}
