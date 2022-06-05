# Maintainer: artoo <artoo@artixlinux.org>

pkgname=power-profiles-daemon-openrc
pkgver=20220503
pkgrel=1
pkgdesc="OpenRC power-profiles-daemon init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-power-profiles-daemon')
depends=('openrc' 'power-profiles-daemon')
conflicts=('init-power-profiles-daemon')
backup=('etc/conf.d/power-profiles-daemon')
source=("power-profiles-daemon.confd"
        "power-profiles-daemon.initd")
sha256sums=('024f6470bfe994ce96de6d550707dff8b73e9713677e13c2ddc82581da825ac6'
            '761305b9cb13425b587ac70205b0b5f19fd59d8e58f75a16c569c4adae4b2f82')

package() {
    install -Dm755 "${srcdir}"/power-profiles-daemon.initd "${pkgdir}"/etc/init.d/power-profiles-daemon
    install -Dm644 "${srcdir}"/power-profiles-daemon.confd "${pkgdir}"/etc/conf.d/power-profiles-daemon
}

