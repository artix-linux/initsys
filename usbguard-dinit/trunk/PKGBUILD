# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=usbguard-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service script for usbguard"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('usbguard' 'dinit')
groups=('dinit-world')
conflicts=('init-usbguard')
provides=('init-usbguard')
source=("usbguard")
sha256sums=('869a807882b65236fdccd2442cc3359e82ba0352ecdbc841f0c6034fa6615d9e')

package() {
    install -Dm644 usbguard "$pkgdir/etc/dinit.d/usbguard"
}
