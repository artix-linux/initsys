# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=openntpd-dinit
pkgver=20211025
pkgrel=2
pkgdesc="dinit service scripts for openntpd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('openntpd' 'dinit')
groups=('dinit-galaxy')
conflicts=('init-openntpd' 'init-timed' 'ntp')
provides=('init-openntpd' 'init-timed')
source=("ntpd")
sha256sums=('0f40e3e726c369278c97121214ea6685db6f57cec4bb3d4b9ac4f477da910729')

package() {
    mkdir -p "$pkgdir/etc/dinit.d"
    install -Dm644 ntpd "$pkgdir/etc/dinit.d"
}
