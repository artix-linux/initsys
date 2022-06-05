# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=rng-tools-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC rng-tools init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'rng-tools')
provides=('init-rng-tools')
conflicts=('init-rng-tools')
source=("rngd.confd"
        "rngd.initd")
sha256sums=('4023c9020947db0bb9572ed739797c297791ac45dbc2d04808a332d907583a59'
            '8932f4536154e821aa82e38c133c64462dca0cd5db968de10d9ada54865420a2')

package() {
    install -Dm755 "$srcdir/rngd.initd" "$pkgdir/etc/init.d/rngd"
    install -Dm644 "$srcdir/rngd.confd" "$pkgdir/etc/conf.d/rngd"
}
