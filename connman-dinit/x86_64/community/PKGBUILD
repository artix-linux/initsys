# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=connman-dinit
pkgver=20211026
pkgrel=1
pkgdesc="dinit service scripts for connman"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('connman' 'dbus-dinit')
groups=('dinit-galaxy')
provides=('init-connman')
conflicts=('init-connman')
source=("connmand")
sha256sums=('7a49047bb91ad83ec8ce452918af5cfba75a3684d8dba2cbd883ecde1ccbc4c6')

package() {
    install -Dm644 connmand "$pkgdir/etc/dinit.d/connmand"
}
