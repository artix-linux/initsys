# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=cyrus-sasl-dinit
pkgver=20211203
pkgrel=1
pkgdesc="dinit service scripts for cyrus-sasl"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('cyrus-sasl' 'dinit')
backup=('etc/dinit.d/config/saslauthd.conf')
conflicts=('init-cyrus-sasl')
provides=('init-cyrus-sasl')
source=("saslauthd"
        "saslauthd.script"
        "saslauthd.conf")
sha256sums=('b2ec769e5478f026596dada92e322e5fb1eccf88d374b0a0f1be49b79ac81a6c'
            '5db8888b846a248257730ab7ff5d3fc06abe295f1415e3f0587b7b5ddbb3c95f'
            '4754b3ebb2a3cffe5553afa9f00f170f37fb7e4041218706cc6fe1928ef2c58c')

package() {
    install -Dm644 saslauthd        "$pkgdir/etc/dinit.d/saslauthd"
    install -Dm644 saslauthd.conf   "$pkgdir/etc/dinit.d/config/saslauthd.conf"
    install -Dm755 saslauthd.script "$pkgdir/etc/dinit.d/scripts/saslauthd"
}
