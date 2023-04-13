# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=seatd-dinit
pkgver=20230412
pkgrel=1
pkgdesc="dinit service scripts for seatd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('seatd' 'dinit')
conflicts=('init-seatd' 'init-logind' 'elogind-dinit')
provides=('init-seatd' 'init-logind' 'elogind-dinit')
source=("seatd" "logind")
sha256sums=('a4384248514fbac7eed9e54996e1396be81daeeb15d67e26ebc4edc80ab30aa0'
            'a5a1cb9de1c12250a7db57ca0e8f38709cad1cf9c94cad630ba2e155ff48b346')

package() {
    install -Dm644 seatd  "$pkgdir/etc/dinit.d/seatd"
    install -Dm644 logind "$pkgdir/etc/dinit.d/logind"
}
