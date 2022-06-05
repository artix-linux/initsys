# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=udpxy-openrc
pkgver=20210505
pkgrel=2
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'udpxy')
provides=('init-udpxy')
conflicts=('init-udpxy')
source=("${pkgname/-openrc/}.initd")
sha256sums=('d4321636be4b1fe138b700f496082261cc44a745276d7f0ccaa656a7912a9068')

package() {
  install -Dm755 "$srcdir/udpxy.initd" "$pkgdir/etc/init.d/udpxy"
}
