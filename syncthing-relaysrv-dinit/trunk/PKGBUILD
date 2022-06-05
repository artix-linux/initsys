# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=syncthing-relaysrv-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for syncthing-relaysrv"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('syncthing-relaysrv' 'dinit')
conflicts=('init-syncthing-relaysrv')
provides=('init-syncthing-relaysrv')
source=("syncthing-relaysrv")
sha256sums=('85597ce6483055b50ecbe18f1e124a5e1cfe6a3ff9e5d7b9f5fb70a5502b8728')

package() {
    install -Dm644 syncthing-relaysrv "$pkgdir/etc/dinit.d/syncthing-relaysrv"
}
