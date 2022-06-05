# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=vnstat-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC vnstat init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'vnstat')
provides=('init-vnstat')
conflicts=('init-vnstat')
backup=('etc/conf.d/vnstatd')
source=("vnstatd.confd"
        "vnstatd.initd")
sha256sums=('e5820c6557cd578faf31c6d5060606e9fe4c024d5f91a90e9b4701c4677fbb5f'
            'e6bd8872705d0a31cb138b4ef9cdba62a7a52f113c486bc3ffacba397b12324b')

package() {
    install -Dm755 "$srcdir/vnstatd.initd" "$pkgdir/etc/init.d/vnstatd"
    install -Dm644 "$srcdir/vnstatd.confd" "$pkgdir/etc/conf.d/vnstatd"
}
