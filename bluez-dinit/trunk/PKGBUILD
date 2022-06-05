# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=bluez-dinit
pkgver=20211026
pkgrel=1
pkgdesc="dinit service scripts for bluez"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('bluez' 'init-dbus')
groups=('dinit-world')
provides=('init-bluez')
conflicts=('init-bluez')
source=("bluetoothd")
sha256sums=('9b4842c351f3018afc4e8c809e65265da9826c6326e3807a8ead9d1d94560a7d')

package() {
    install -Dm644 bluetoothd "$pkgdir/etc/dinit.d/bluetoothd"
}
