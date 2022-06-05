# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=elogind-dinit
pkgver=20211030
pkgrel=1
pkgdesc="dinit service scripts for elogind"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('elogind' 'dinit' 'dbus-dinit')
provides=('init-elogind' 'init-logind')
conflicts=('init-elogind' 'init-logind')
groups=('dinit-system')
source=("elogind" "logind")
sha256sums=('6cb7124c0313879f944b83856dc7913afbef5e854a6acfe0101a4c30497c088e'
            'dd3401a038ffd16e9377fd80691210adc943a148effc5056a5424800ca00140c')

package() {
    install -Dm644 elogind "$pkgdir/etc/dinit.d/elogind"
    install -Dm644 logind  "$pkgdir/etc/dinit.d/logind"

    # Add default
    install -d "$pkgdir/etc/dinit.d/boot.d"
    ln -sf ../logind "$pkgdir/etc/dinit.d/boot.d"
}
