# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=stunnel-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for stunnel"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('stunnel' 'dinit')
conflicts=('init-stunnel')
provides=('init-stunnel')
source=("stunnel" "stunnel.script")
sha256sums=('8a5856e84dbef18c4c3b0ac43846bc98c2e80ce8868b4662f3db87ce145f67fe'
            'd138a4506abb5c088398a2d241c4dda2fbf03a43b5c18a580c3395101195174e')

package() {
    install -Dm644 stunnel        "$pkgdir/etc/dinit.d/stunnel"
    install -Dm755 stunnel.script "$pkgdir/etc/dinit.d/scripts/stunnel"
}
