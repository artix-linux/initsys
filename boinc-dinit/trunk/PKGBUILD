# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=boinc-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for boinc"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('boinc' 'dinit')
conflicts=('init-boinc')
provides=('init-boinc')
source=("boinc")
sha256sums=('41151b15a0adde543edc970da162725479738d1e155899ed5acbe425f0d5d4b7')

package() {
    install -Dm644 boinc "$pkgdir/etc/dinit.d/boinc"
}
