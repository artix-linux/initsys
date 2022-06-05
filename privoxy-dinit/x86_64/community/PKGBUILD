# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=privoxy-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for privoxy"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('privoxy' 'dinit')
conflicts=('init-privoxy')
provides=('init-privoxy')
source=("privoxy")
sha256sums=('bcdd398ec6e70713f13ca6bd429cac072e880109aaec40f4560d5bef0d7af397')

package() {
    install -Dm644 privoxy "$pkgdir/etc/dinit.d/privoxy"
}
