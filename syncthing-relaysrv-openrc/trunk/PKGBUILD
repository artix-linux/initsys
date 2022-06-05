# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=syncthing-relaysrv-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC syncthing-relaysrv init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'syncthing-relaysrv')
provides=('init-syncthing-relaysrv')
conflicts=('init-syncthing-relaysrv')
backup=('etc/conf.d/strelaysrv')
source=('strelaysrv.'{initd,confd})
sha256sums=('9e9c5e7c84f092a7086e323c6a3ae07942edfb9157314d414b95dfe351087a05'
            '8ae5fb440478f93a9450a723249729b814056e9447b2ea8db1c32b9eb8ccee47')

package() {
  cd "$srcdir"
  install -Dm755 strelaysrv.initd "$pkgdir"/etc/init.d/strelaysrv
  install -Dm644 strelaysrv.confd "$pkgdir"/etc/conf.d/strelaysrv
}
