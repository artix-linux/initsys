# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=intel-undervolt-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC script for intel-undervolt"
arch=('x86_64')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'intel-undervolt')
provides=('init-intel-undervolt')
conflicts=('init-intel-undervolt')
source=('intel-undervolt.initd')
b2sums=('2e38d9c7887aa41a5eb9453c427311107f328c206869d8fbace76f4a18abaa63ed5b857687d6e70a8692a783bf7deb5537ac63b9d9bbef77d5697348a53c2d99')

package() {
  cd "$srcdir"
  install -Dm755 intel-undervolt.initd "$pkgdir"/etc/init.d/intel-undervolt
}

# vim:set ts=2 sw=2 et:
