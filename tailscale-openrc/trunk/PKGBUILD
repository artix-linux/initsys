# Maintainer: Nathan <ndowens@artixlinux.org>
pkgname=tailscale-openrc
pkgver=20220615
pkgrel=1
pkgdesc="OpenRC init script for tailscale"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('tailscale' 'openrc')
provides=('init-tailscale')
conflicts=('init-tailscale')
source=('tailscaled'{,.confd})
sha256sums=('3e064cd38f3b832887eed86f440d650af2445ad9d8bc74600d259cd910d8e4bb'
            '06f04d9add861580c420b6207525bfc21112d9b1c9ad9e55caf77fc06f278095')

package() {
  cd "$srcdir"

  install -Dm755 tailscaled -t "$pkgdir"/etc/init.d
  install -Dm644 tailscaled.confd "$pkgdir"/etc/conf.d/tailscaled
}

# vim:set ts=2 sw=2 et:
