# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=spotifyd-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for spotifyd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('spotifyd' 'dinit')
conflicts=('init-spotifyd')
provides=('init-spotifyd')
source=("spotifyd")
sha256sums=('c0ad745a7c83bcec3f665231ab7189520a5250cd1cf2995bc32f70400adcd138')

package() {
    install -Dm644 spotifyd "$pkgdir/etc/dinit.d/spotifyd"
}
