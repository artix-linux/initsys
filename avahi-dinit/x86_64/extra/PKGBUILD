# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=avahi-dinit
pkgver=20211026
pkgrel=1
pkgdesc="dinit service scripts for avahi"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('avahi' 'init-dbus')
groups=('dinit-world')
provides=('init-avahi')
conflicts=('init-avahi')
source=("avahi-daemon")
sha256sums=('9a16f8936cc1d3c04d646bcb626073cc4aefdab728d572866e1e0c44246ea615')

package() {
    install -Dm644 avahi-daemon "$pkgdir/etc/dinit.d/avahi-daemon"
}
