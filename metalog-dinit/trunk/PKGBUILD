# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=metalog-dinit
pkgver=20211026
pkgrel=1
pkgdesc="dinit service scripts for metalog"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('metalog' 'dinit')
conflicts=('init-metalog')
provides=('init-metalog')
source=("metalog")
sha256sums=('2749b4ae9ff763cb108f085ea6fe210e86e2b2118b45d0af679ff1b36d59426a')

package() {
    install -Dm644 metalog "$pkgdir/etc/dinit.d/metalog"
}
