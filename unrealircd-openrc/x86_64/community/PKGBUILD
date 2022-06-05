# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=unrealircd-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'unrealircd')
provides=('init-unrealircd')
conflicts=('init-unrealircd')
source=("${pkgname/-openrc/}.initd")
sha256sums=('d4ddaaad898ccb7ca711cce1baf0ce145804731ee3acb18f21a43c5f3af6bea7')

package() {
  install -Dm755 "$srcdir/unrealircd.initd" "$pkgdir/etc/init.d/unrealircd"
}
