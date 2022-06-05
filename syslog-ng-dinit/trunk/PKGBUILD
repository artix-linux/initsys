# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=syslog-ng-dinit
pkgver=20211027
pkgrel=1
pkgdesc="dinit service scripts for syslog-ng"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('syslog-ng' 'dinit')
conflicts=('init-syslog-ng')
provides=('init-syslog-ng')
source=("syslog-ng")
sha256sums=('f28a5bde5547752902cc0e440ef82577014fc46581f148f0c734fae5f230c503')

package() {
    install -Dm644 syslog-ng "$pkgdir/etc/dinit.d/syslog-ng"
}
