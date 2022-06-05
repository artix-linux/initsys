# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=bumblebee-openrc
pkgver=20210506
pkgrel=1
pkgdesc="OpenRC bumblebee init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('bumblebee-init')
depends=('openrc' 'bumblebee')
conflicts=('bumblebee-init')
backup=('etc/conf.d/bumblebee')
source=("bumblebee.confd"
        "bumblebee.initd")
sha256sums=('9e0287f542cff0fd3452a0c3d6d427a3404706c93ac9a00f4d99fe52ed596d75'
            '9edfc6fa88d72f2c7faf6f7c39f7a416ee33cf1cd558626d55268e99413a0876')

package() {
    install -Dm755 "${srcdir}"/bumblebee.initd "${pkgdir}"/etc/init.d/bumblebee
    install -Dm644 "${srcdir}"/bumblebee.confd "${pkgdir}"/etc/conf.d/bumblebee
}
