# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=trojan-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC script for trojan"
arch=('x86_64')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'trojan')
provides=('init-trojan')
conflicts=('init-trojan')
source=('trojan.initd')
b2sums=('8c021142a6c59dc2fde43bdc75d80c784600583aa997d4bc74539963ec41bdb7a15e57eb7b31ff4ea69e6d3f0034df8bf04fa3f971ca927d306bd9fe12ef9ab5')

package() {
  cd "$srcdir"
  install -Dm755 trojan.initd "$pkgdir"/etc/init.d/trojan
}

# vim:set ts=2 sw=2 et:
