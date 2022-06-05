# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=postfix-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for postfix"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('postfix' 'dinit')
provides=('init-postfix')
conflicts=('init-postfix')
source=("postfix" "postfix.script")
sha256sums=('702640b89b7633ff86ef4714e2b506c6d7062099183ee542673111b3672a192a'
            '1300990a332330abb3be608df3b6105024ab056901813f4bdddb8586a66a9522')

package() {
    install -Dm644 postfix        "$pkgdir/etc/dinit.d/postfix"
    install -Dm755 postfix.script "$pkgdir/etc/dinit.d/scripts/postfix"
}
