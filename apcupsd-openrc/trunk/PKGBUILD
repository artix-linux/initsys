# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=apcupsd-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC apcupsd init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
conflicts=('init-apcupsd')
provides=('init-apcupsd')
depends=('openrc' 'apcupsd')
source=("apcupsd.initd"
        "apcupsd.powerfail.initd")
sha256sums=('5fd474027ddb56c0c5974d4d7ca0e568f3167b90fbd40001f6cb85035d4e7481'
            'ca6c0f83d239b98a3cf75dea01dce2bbd01cee244e1e47cf983c1ff101b65e49')

package() {
	install -Dm755 "$srcdir/apcupsd.initd" "$pkgdir/etc/init.d/apcupsd"
	install -Dm755 "$srcdir/apcupsd.powerfail.initd" "$pkgdir/etc/init.d/apcupsd.powerfail"
}
