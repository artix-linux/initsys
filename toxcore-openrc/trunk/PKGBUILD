# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=toxcore-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC tox init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'toxcore')
provides=('init-toxcore')
conflicts=('init-toxcore')
source=("tox.confd"
        "tox.initd")
sha256sums=('eb0aa3b25232a64971c6b39799c384577cf85ffe16ec41119b6b4e8336649cd5'
            '1d2338543e40c5452cfbc27b997cf5fc2140db45b27a20b48136bf6781fb4595')

package() {
	install -Dm755 "$srcdir/tox.initd" "$pkgdir/etc/init.d/tox"
	install -Dm644 "$srcdir/tox.confd" "$pkgdir/etc/conf.d/tox"
}
