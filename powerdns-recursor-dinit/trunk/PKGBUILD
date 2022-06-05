# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=powerdns-recursor-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for powerdns-recursor"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('powerdns-recursor' 'dinit')
conflicts=('init-powerdns-recursor')
provides=('init-powerdns-recursor')
source=("pdns-recursor" "pdns-recursor.script")
sha256sums=('194e9b441b5b89cef8b93d0f39968f89b1f1505f2bf658fa5868e43968fab9c0'
            '53b8138eecd046a2ff1ac7c3069d6fe17fdfbc7d96b8dc6bba022f6f456a957d')

package() {
    install -Dm644 pdns-recursor        "$pkgdir/etc/dinit.d/pdns-recursor"
    install -Dm755 pdns-recursor.script "$pkgdir/etc/dinit.d/scripts/pdns-recursor"
}
