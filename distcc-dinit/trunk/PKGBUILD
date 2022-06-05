# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=distcc-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for distcc"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('distcc' 'dinit')
conflicts=('init-distcc')
provides=('init-distcc')
backup=('etc/dinit.d/config/distcc.conf')
source=("distcc" "distcc.conf" "distcc.script")
sha256sums=('2a78b63f8f2737e88092a50abeeb5927061a3d045ca5ba6e1cc01179d820e8fd'
            '6419d7377aa55bf3848fe654df0fb19cf97419335d611fd1c9e028670a49d7e3'
            'f6a83fa54209eef876f7ee92ad3d6271448a705abb8a8a9ec092772f6b8f5a4a')

package() {
    install -Dm644 distcc        "$pkgdir/etc/dinit.d/distcc"
    install -Dm644 distcc.conf   "$pkgdir/etc/dinit.d/config/distcc.conf"
    install -Dm755 distcc.script "$pkgdir/etc/dinit.d/scripts/distcc"
}
