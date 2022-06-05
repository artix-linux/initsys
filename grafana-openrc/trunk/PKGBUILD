# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=grafana-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC grafana init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'grafana')
provides=('init-grafana')
conflicts=('init-grafana')
backup=('etc/conf.d/grafana')
source=("grafana.confd"
        "grafana.initd")
sha256sums=('5b9e125f2648ed98125097770b609dcce543443f0862b99c0653f55b3b9be895'
            '6637505d7030172e80ea3bc153a041b7e9fa6a068bf38ea26e8e1dc61b81ffed')

package() {
    install -Dm755 "$srcdir/grafana.initd" "$pkgdir/etc/init.d/grafana"
    install -Dm644 "$srcdir/grafana.confd" "$pkgdir/etc/conf.d/grafana"
}
