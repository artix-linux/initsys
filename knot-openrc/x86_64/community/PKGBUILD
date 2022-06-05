# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=knot-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC knot init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'knot')
provides=('init-knot')
conflicts=('init-knot')
source=("knot.confd"
        "knot.initd")
sha256sums=('ff384d428c9e67139ed21b0c78eabf6a26d96f31775f6143ce0c4f9c4f6beaf3'
            '71386b03cb4df4b05b12a023603e308c57122568de2290004ea480f48696550a')

package() {
	install -Dm755 "$srcdir/knot.initd" "$pkgdir/etc/init.d/knot"
	install -Dm644 "$srcdir/knot.confd" "$pkgdir/etc/conf.d/knot"
}
