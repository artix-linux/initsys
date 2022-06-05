# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=dnsmasq-dinit
pkgver=20211206
pkgrel=1
pkgdesc="dinit service scripts for dnsmasq"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('dnsmasq' 'dinit' 'dbus-dinit')
provides=('init-dnsmasq')
conflicts=('init-dnsmasq')
source=("dnsmasq")
sha256sums=('9aeb169d0e5cf67f5211a695b9fabb4b3ced4643bf536ae3eaf06426bb974e9a')

package() {
    install -Dm644 dnsmasq "$pkgdir/etc/dinit.d/dnsmasq"
}
