# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=power-profiles-daemon-dinit
pkgver=20220514
pkgrel=1
pkgdesc="dinit service scripts for power-profiles-daemon"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('power-profiles-daemon' 'dbus-dinit' 'dinit')
conflicts=('init-power-profiles-daemon')
provides=('init-power-profiles-daemon')
source=("power-profiles-daemon")
sha256sums=('531ec88b3bff3fd9b55fbedb9051da63c9df716eb8d021ead1989528808ec4cb')

package() {
    install -Dm644 power-profiles-daemon "$pkgdir/etc/dinit.d/power-profiles-daemon"
}
