# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=brltty-dinit
pkgver=20211030
pkgrel=1
pkgdesc="dinit service scripts for brltty"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('brltty' 'dinit')
provides=('init-brltty')
conflicts=('init-brltty')
source=("brltty" "brltty.script")
sha256sums=('46433f66d7407d696167f0ba40217238b821643ba1110bb367351fc77ea52e20'
            '8eb8b413dff0c3791c554c012a82731ce05ecf4442748a477246963753f9d717')

package() {
    install -Dm644 brltty        "$pkgdir/etc/dinit.d/brltty"
    install -Dm755 brltty.script "$pkgdir/etc/dinit.d/scripts/brltty"
}
