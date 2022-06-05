# Maintainer: artoo <artoo@artixlinux.org>

pkgname=dbus-openrc
pkgver=20210418
pkgrel=2
pkgdesc="OpenRC dbus init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
depends=('dbus' 'openrc')
provides=('init-dbus')
conflicts=('init-dbus')
source=('dbus.initd'
        'dbus-reload.hook'
        '80-dbus')
sha256sums=('3801358d1fe65db3711851c4a2d7c491c8750c899d8effdf37eb64d34683e91b'
            '517cb12a30f84ba9580532d5485ce219ad96668480db99fcd4954c7017a0ea47'
            '6d637acae40368db9e7c005b2e53483882014caef281fe9e801633ba7cc3b7dd')

package() {
    install -Dm755 "${srcdir}"/dbus.initd "${pkgdir}"/etc/init.d/dbus

    install -d "${pkgdir}"/etc/runlevels/default
    ln -sf /etc/init.d/dbus "${pkgdir}"/etc/runlevels/default/dbus

    install -Dt "${pkgdir}"/usr/share/libalpm/hooks -m644 *.hook

    install -Dm755 "${srcdir}"/80-dbus "${pkgdir}"/etc/X11/xinit/xinitrc.d/80-dbus.sh
}
