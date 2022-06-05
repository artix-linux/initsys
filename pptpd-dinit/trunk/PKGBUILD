# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=pptpd-dinit
pkgver=20211105
pkgrel=2
pkgdesc="dinit service scripts for pptpd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('pptpd' 'dinit')
conflicts=('init-pptpd')
provides=('init-pptpd')
source=("pptpd")
sha256sums=('8129a451498cf58a09fe280c6246d4c931fb851b45e30f34b97e318f9f81bd11')

package() {
    install -Dm644 pptpd "$pkgdir/etc/dinit.d/pptpd"
}
