# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=networkmanager-dinit
pkgver=20211026
pkgrel=1
pkgdesc="dinit service scripts for networkmanager"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('networkmanager' 'dbus-dinit')
conflicts=('init-networkmanager')
provides=('init-networkmanager')
source=("NetworkManager")
sha256sums=('0ce92f507c31bfaa5a506cb223fcce160d9bb8632317f36e88b851f4504ca6e1')

package() {
    install -Dm644 NetworkManager "$pkgdir/etc/dinit.d/NetworkManager"
}
