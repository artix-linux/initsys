# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=mopidy-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for mopidy"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('mopidy' 'dinit')
conflicts=('init-mopidy')
provides=('init-mopidy')
source=("mopidy")
sha256sums=('5bc53d7d7567291143c508acb707456c11c2fbbc085f0907f4c4d532867836ed')

package() {
    install -Dm644 mopidy "$pkgdir/etc/dinit.d/mopidy"
}
