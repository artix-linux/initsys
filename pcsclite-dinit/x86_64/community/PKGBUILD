# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=pcsclite-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for pcsclite"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('pcsclite' 'dinit')
conflicts=('init-pcsclite')
provides=('init-pcsclite')
source=("pcscd")
sha256sums=('43988d5bf5e0a8cd79a508a11d572d1fb2a771d9571ae85515ed6e6fb9c3f4be')

package() {
    install -Dm644 pcscd "$pkgdir/etc/dinit.d/pcscd"
}
