# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=consul-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC consul init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'consul')
provides=('init-consul')
conflicts=('init-consul')
backup=('etc/conf.d/consul')
source=("consul.confd"
        "consul.initd")
sha256sums=('9a96a8e930e3753e212307c9d3d474b918e79062352a87f09b7e7bf43a108450'
            '9e3eeb74b358bdf21e289d0b4a164b96f36b35253c3ed9c9a00ccc0a4afd5df5')

package() {
	install -Dm755 "$srcdir/consul.initd" "$pkgdir/etc/init.d/consul"
	install -Dm644 "$srcdir/consul.confd" "$pkgdir/etc/conf.d/consul"
}
