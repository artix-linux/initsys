# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=shairport-sync-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC script for shairport-sync"
arch=('x86_64')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'shairport-sync' 'avahi-openrc')
provides=('init-shairport-sync')
conflicts=('init-shairport-sync')
source=(shairport-sync)
b2sums=('51284d6beff69162511e66f3d4181f82d877fbf4ae424ff1755a18e38de6470cfbf0eaae00ad0fb9a1c9164121a917ac4a07b5328e275866b482e1f86bb22aaf')

package() {
  cd "$srcdir"
  install -Dm755 shairport-sync -t "$pkgdir"/etc/init.d
}

# vim:set ts=2 sw=2 et:
