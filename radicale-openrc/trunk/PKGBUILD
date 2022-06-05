# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=radicale-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'radicale')
provides=('init-radicale')
conflicts=('init-radicale')
source=("${pkgname/-openrc/}.initd")
sha256sums=('a04ee36d917e3062ddef74d50a9568f482f74e13a57ec817337b54442495ed56')

package() {
  install -Dm755 "$srcdir/radicale.initd" "$pkgdir/etc/init.d/radicale"
}
