# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=bolt-openrc
pkgver=20210506
pkgrel=1
pkgdesc="OpenRC script for bolt"
arch=('x86_64')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('init-bolt')
depends=('openrc' 'bolt')
conflicts=('init-bolt')
source=('boltd')
b2sums=('c33db5d1c573ec1dac64feee109e8acd364d949853e95b47a4f4b690d72cfc65178eb82755dcf1c9dc8c84692e25bfb52cd14097fad1f685b55a1aa1728f7758')

package() {
  install -Dm755 "$srcdir"/boltd -t "$pkgdir"/etc/init.d
}

# vim:set ts=2 sw=2 et:
