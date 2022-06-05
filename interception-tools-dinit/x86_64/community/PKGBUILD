# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=interception-tools-dinit
pkgver=20211101
pkgrel=1
pkgdesc="dinit service scripts for interception-tools"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('interception-tools' 'dinit')
conflicts=('init-interception-tools')
provides=('init-interception-tools')
source=("udevmon")
sha256sums=('1b00d244bcd6f69d3f45f75009c48f2376c5446835e46d3b7dc05f47e558d362')

package() {
    install -Dm644 udevmon "$pkgdir/etc/dinit.d/udevmon"
}
