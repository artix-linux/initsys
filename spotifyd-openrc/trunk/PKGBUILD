# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=spotifyd-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC script for spotifyd"
arch=('x86_64')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'spotifyd')
provides=('init-spotifyd')
conflicts=('init-spotifyd')
source=('spotifyd')
b2sums=('502fa16d4ddff7cda201d9413519b520c5628dfe19f56c4ab75edeff4840f8722fedca1b6898ca46f374f1eac79ee853d965b80022cccad0e4dbc701a661df12')

package() {
  cd "$srcdir"
  install -Dm755 spotifyd -t "$pkgdir"/etc/init.d/
}

# vim:set ts=2 sw=2 et:
