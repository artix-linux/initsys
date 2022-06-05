# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=samba-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for samba"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('samba' 'dinit')
conflicts=('init-samba')
provides=('init-samba')
source=("smbd"
        "nmbd"
        "samba-pre")
sha256sums=('1c0e8c1ff66fd12a4c7474d1eddba3834fb3090cca70f4875015d5e31af4c0e5'
            'd87cd6b183b6fc09f61df84c9cd7774ed4cca4194ad23e2a8b8416807459a82b'
            'ba176ce8ed70353b869574c5b38cf134150f2608d92e57a85a1e28f6308bfaec')

package() {
    install -Dm644 smbd      "$pkgdir/etc/dinit.d/smbd"
    install -Dm644 nmbd      "$pkgdir/etc/dinit.d/nmbd"
    install -Dm644 samba-pre "$pkgdir/etc/dinit.d/samba-pre"
}
