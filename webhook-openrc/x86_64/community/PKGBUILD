# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=webhook-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'webhook')
provides=('init-webhook')
conflicts=('init-webhook')
source=("${pkgname/-openrc/}.initd")
sha256sums=('109d9b223cfd497301f46c73c30b485ad44e3af5c32ddddff5b20219bb851535')

package() {
  install -Dm755 "$srcdir/webhook.initd" "$pkgdir/etc/init.d/webhook"
}
