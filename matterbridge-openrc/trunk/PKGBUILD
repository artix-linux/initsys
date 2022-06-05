# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=matterbridge-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC script for matterbridge"
arch=('x86_64')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'matterbridge')
provides=('init-matterbridge')
conflicts=('init-matterbridge')
source=('matterbridge.initd')
b2sums=('eef7511d82fa5e549fa3297b59e29543a9328d07de5ef7e9effb41694d4a6cdf2a9f03b2156c553867d9d88579f14dc89b17b381f24a6673418a27a1b100abff')

package() {
  cd "$srcdir"
  install -Dm755 matterbridge.initd "$pkgdir"/etc/init.d/matterbridge
}

# vim:set ts=2 sw=2 et:
