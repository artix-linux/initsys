# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=openntpd-openrc
pkgver=20210505
pkgrel=3
pkgdesc="OpenRC openntpd init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('init-openntpd' 'init-timed')
depends=('openrc' 'openntpd')
conflicts=('ntp' 'init-timed' 'init-openntpd')
backup=('etc/conf.d/ntpd')
source=("ntpd".{confd,initd})
sha256sums=('91fb1497b3a6ef0bb3a3d5baefdff801d8ff1cba27aaf742303415550814a09b'
            '6aca75ce5a686e4ae5907fa16ca5ea9db43ba28690fb8e581721a22a31b02aaf')

package() {
    install -Dm755 "$srcdir"/ntpd.initd "$pkgdir"/etc/init.d/ntpd
    install -Dm644 "$srcdir"/ntpd.confd "$pkgdir"/etc/conf.d/ntpd
}
