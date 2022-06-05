# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=backlight-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for backlight"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('dinit')
conflicts=('init-backlight')
provides=('init-backlight')
source=("backlight" "backlight.script")
sha256sums=('7447e517186e6a3372984f7d17f9cfb2f268ad378dba36d321f8004a1b535a63'
            '2af6767979264b9024c565351e26ce0570e2734a84c1eb914596e8c54d4566fb')

package() {
    install -Dm644 backlight        "$pkgdir/etc/dinit.d/backlight"
    install -Dm755 backlight.script "$pkgdir/etc/dinit.d/scripts/backlight"
}
