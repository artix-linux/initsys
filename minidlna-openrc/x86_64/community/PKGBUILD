# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>
# Contributor: nous <nous@artixlinux.org>

pkgname=minidlna-openrc
pkgver=20211107
pkgrel=1
pkgdesc="OpenRC minidlna init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('openrc-minidlna')
depends=('openrc' 'minidlna')
provides=('init-minidlna')
conflicts=('init-minidlna')
backup=('etc/conf.d/minidlna')
source=("minidlna.confd"
        "minidlna.initd")
sha256sums=('67603d65c6bd3918255f050cb5cfd6fc1373b024bca1ce728f03491a90d79e19'
            'a6fccc2ecf994bac554ad8b480234b8cfa535f48974f56359bb3aa4d5a1c3b4e')

package() {
	install -Dm755 "$srcdir/minidlna.initd" "$pkgdir/etc/init.d/minidlna"
	install -Dm644 "$srcdir/minidlna.confd" "$pkgdir/etc/conf.d/minidlna"
}
