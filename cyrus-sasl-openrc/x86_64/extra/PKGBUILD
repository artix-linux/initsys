# Maintainer: artoo <artoo@artixlinux.org>

pkgname=cyrus-sasl-openrc
pkgver=20210505
pkgrel=2
pkgdesc="OpenRC cyrus-sasl init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-cyrus-sasl')
depends=('openrc' 'cyrus-sasl')
conflicts=('init-cyrus-sasl')
source=("saslauthd.initd")
sha256sums=('9b5f5c652cf354e73b04b4f410b6b7303d5b1d76723ec4bf93d956ea14340e9a')

package() {
	install -Dm755 "${srcdir}"/saslauthd.initd "${pkgdir}"/etc/init.d/saslauthd
}
