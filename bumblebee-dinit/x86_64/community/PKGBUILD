# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=bumblebee-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for bumblebee"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('bumblebee' 'dinit')
conflicts=('init-bumblebee')
provides=('init-bumblebee')
source=("bumblebeed")
sha256sums=('21c34e6c1030e431e5a24ba324e41a164566e0cc7741cd41a285d5b4bc1d1f4c')

package() {
    install -Dm644 bumblebeed "$pkgdir/etc/dinit.d/bumblebeed"
}
