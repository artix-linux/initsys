# Maintainer: nous@artixlinux.org

pkgname=uptimed-openrc
pkgver=20220601
pkgrel=2
pkgdesc="OpenRC uptimed init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'uptimed')
provides=('init-uptimed')
conflicts=('init-uptimed')
source=("uptimed.initd")
sha256sums=('3bc0a693a2d09fe7e884c961dde6d37cdb67abad29df3594e43bf016bb288855')

package() {
	install -Dm755 "$srcdir/uptimed.initd" "$pkgdir/etc/init.d/uptimed"
}
