# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=matterbridge-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for matterbridge"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('matterbridge' 'dinit')
conflicts=('init-matterbridge')
provides=('init-matterbridge')
source=("matterbridge")
sha256sums=('61a28de5ce972e3f1c7c3f40c14a953148f3e391020a83f2eb871c90573b5d19')

package() {
    install -Dm644 matterbridge "$pkgdir/etc/dinit.d/matterbridge"
}
