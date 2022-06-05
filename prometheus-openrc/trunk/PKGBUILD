# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=prometheus-openrc
pkgver=20210505
pkgrel=2
pkgdesc="OpenRC prometheus init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-prometheus')
depends=('openrc' 'prometheus')
conflicts=('init-prometheus')
backup=('etc/conf.d/prometheus')
source=("prometheus".{confd,initd})
sha256sums=('940f1a3ad08f0eb370951b1a42c29a9217cba9ae2f5cb6cc675bdec1d51e8309'
            'fc364f22e586a80c1541049d7f18ea5f6068545403227519fd4ebc72968bc5af')

package() {
    install -Dm755 "$srcdir/prometheus.initd" "$pkgdir/etc/init.d/prometheus"
    install -Dm644 "$srcdir/prometheus.confd" "$pkgdir/etc/conf.d/prometheus"
}
