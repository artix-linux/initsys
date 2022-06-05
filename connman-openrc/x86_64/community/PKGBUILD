# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=connman-openrc
pkgver=20210506
pkgrel=1
pkgdesc="OpenRC connman init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('init-connman')
depends=('openrc' 'connman')
conflicts=('init-connman')
backup=('etc/conf.d/connmand')
source=("connmand.confd"
        "connmand.initd")
sha256sums=('e92c5c58ab45f85b6da4f7b153fd2f7ad9aa95d96f7d684cbffd3779dca647e3'
            '5cc966e53e0bfe2b6e551b629a777948d8dfd2de8c20ac6979630692a0800791')

package() {
    install -Dm755 "${srcdir}"/connmand.initd "${pkgdir}"/etc/init.d/connmand
    install -Dm644 "${srcdir}"/connmand.confd  "${pkgdir}"/etc/conf.d/connmand
}
