# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=hostapd-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for hostapd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('hostapd' 'dinit')
conflicts=('init-hostapd')
provides=('init-hostapd')
source=("hostapd")
sha256sums=('db52ddc534470769dee3d28d021dafb3b8a6cd1b9d8aefc17d587c97bbb50ac0')

package() {
    install -Dm644 hostapd "$pkgdir/etc/dinit.d/hostapd"
}
