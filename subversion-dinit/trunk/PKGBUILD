# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=subversion-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for subversion"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('subversion' 'dinit')
conflicts=('init-subversion')
provides=('init-subversion')
source=("svnserve")
sha256sums=('da037e1aab6144427d9ce870cb146bb7965da979473c794e7b8593a33605da10')

package() {
    install -Dm644 svnserve "$pkgdir/etc/dinit.d/svnserve"
}
