# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=nvidia-utils-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for nvidia-utils"
arch=('any')
url="https://artixlinux.org"
groups=('dinit-world')
provides=('init-nvidia-utils')
conflicts=('init-nvidia-utils')
depends=('nvidia-utils' 'dinit')
makedepends=('git')
source=('nvidia-persistenced')
sha256sums=('68b09d191623e4834bd2ae0bdf041f8f3df7bc9de06a7ae7fe678d3c2fea9714')

package() {
    install -Dm644 nvidia-persistenced "$pkgdir/etc/dinit.d/nvidia-persistenced"
}
