# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=spice-vdagent-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'spice-vdagent')
provides=('init-spice-vdagent')
conflicts=('init-spice-vdagent')
backup=("etc/conf.d/${pkgname/-openrc/}")
source=("${pkgname/-openrc/}.initd"
	"${pkgname/-openrc/}.confd")
md5sums=('e8df29023501681fd9fe08af395bf077'
         'e18b8257f7a7b6b1c5e4044566d9ba31')

package() {
  install -Dm755 "$srcdir/spice-vdagent.initd" "$pkgdir/etc/init.d/spice-vdagent"
  install -Dm644 "$srcdir/spice-vdagent.confd" "$pkgdir/etc/conf.d/spice-vdagent"
}
