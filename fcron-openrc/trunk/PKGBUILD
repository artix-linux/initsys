# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=fcron-openrc
pkgver=20210505
pkgrel=2
pkgdesc="OpenRC fcron init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('init-fcron' 'init-cron')
depends=('openrc' 'fcron')
conflicts=('cronie' 'init-fcron' 'init-cron')
source=("fcron".{initd,confd})
sha256sums=('b7b7a3cc390fe8ab7eb2b9b7baa5a3f3aac085dde831be3516d0677b4f11da2b'
            'cf64be3aed14f6649df3b8d2100e097baca4117d81e0a3b93c42f9a65082921c')

package() {
    install -Dm755 "$srcdir/fcron.initd" "$pkgdir/etc/init.d/fcron"
    install -Dm644 "$srcdir/fcron.confd" "$pkgdir/etc/conf.d/fcron"
}
