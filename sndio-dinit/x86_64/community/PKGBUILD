# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=sndio-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for sndio"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('sndio' 'dinit')
conflicts=('init-sndio')
provides=('init-sndio')
source=("sndiod")
sha256sums=('d564b9792e572b8870c1e8baf5c51e41e22adde24b9b8762586350db645a3bfa')

package() {
    install -Dm644 sndiod "$pkgdir/etc/dinit.d/sndiod"
}
