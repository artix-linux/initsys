# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=wpa_supplicant-dinit
pkgver=20211028
pkgrel=1
pkgdesc="dinit service scripts for wpa_supplicant"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-system')
depends=('wpa_supplicant' 'dinit')
provides=('init-wpa_supplicant')
conflicts=('init-wpa_supplicant')
backup=('etc/dinit.d/config/wpa_supplicant.conf')
source=("wpa_supplicant" "wpa_supplicant.script" "wpa_supplicant.conf")
sha256sums=('8ca225590dbc6a590afc2d7eb74ab56a5f63ccb80c21c01a8ed84919ff2b531c'
            '6431e6ab9b5332a39291bbc4253cf823a8912b3e1cd4a6cb4a3f53893c5e8d77'
            'ad5929875a33aef2bd3a98b32a98a175ce3171daba0e46cf270b12c6b5c5e51a')

package() {
    install -Dm644 wpa_supplicant        "$pkgdir/etc/dinit.d/wpa_supplicant"
    install -Dm644 wpa_supplicant.conf   "$pkgdir/etc/dinit.d/config/wpa_supplicant.conf"
    install -Dm755 wpa_supplicant.script "$pkgdir/etc/dinit.d/scripts/wpa_supplicant"
}
