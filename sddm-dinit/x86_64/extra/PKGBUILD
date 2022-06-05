# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=sddm-dinit
pkgver=20211026
pkgrel=3
pkgdesc="dinit service scripts for sddm"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('sddm' 'init-logind')
provides=('init-sddm' 'init-displaymanager')
conflicts=('init-sddm' 'init-displaymanager')
source=("sddm" "sddm.script")
sha256sums=('9947664263d284e65b2da0296c20dec65ebfe3f5d6d2d9e2450719de32a74e3e'
            '7dc7739987cb0b70adf01cc1cbcccfcbfc1cc06f34eb2d32659806200512ac5f')

package() {
    install -Dm644 sddm        "$pkgdir/etc/dinit.d/sddm"
    install -Dm755 sddm.script "$pkgdir/etc/dinit.d/scripts/sddm"
}
