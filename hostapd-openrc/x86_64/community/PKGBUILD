# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=hostapd-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC hostapd init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'hostapd')
provides=('init-hostapd')
conflicts=('init-hostapd')
backup=('etc/conf.d/hostapd')
source=("hostapd.confd"
        "hostapd.initd")
sha256sums=('6c14e88b14bb9a93d2dca69239d829f435e93180e621319aeed0f3987290dfba'
            'f5d32b21e0856b0ffcbe61815640c92b4c22a5bc3ee5afd05e8bd040d2c8dd34')

package() {
    install -Dm755 "$srcdir/hostapd.initd" "$pkgdir/etc/init.d/hostapd"
    install -Dm644 "$srcdir/hostapd.confd" "$pkgdir/etc/conf.d/hostapd"
}
