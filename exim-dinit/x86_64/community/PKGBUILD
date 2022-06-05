# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=exim-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for exim"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('exim' 'dinit')
conflicts=('init-exim')
provides=('init-exim')
backup=('etc/dinit.d/config/exim.conf')
source=("exim" "exim.conf" "exim.script")
sha256sums=('ab011994c8ee59eba281f0401fe96b269a22bab608030a52acce690fa0203712'
            'f06161dc7269838b202215397de6c4de2cb827039fde4ddd58000548ff05cc6b'
            'f3cbcb91ad0ab499059a00ebab309bc593fb4db82d4518345a4974ffaad5c265')

package() {
    install -Dm644 exim        "$pkgdir/etc/dinit.d/exim"
    install -Dm644 exim.conf   "$pkgdir/etc/dinit.d/config/exim.conf"
    install -Dm755 exim.script "$pkgdir/etc/dinit.d/scripts/exim"
}
