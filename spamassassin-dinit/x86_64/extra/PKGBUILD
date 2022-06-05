# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=spamassassin-dinit
pkgver=20211030
pkgrel=1
pkgdesc="dinit service script for spamassassin"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('spamassassin' 'dinit')
groups=('dinit-world')
conflicts=('init-spamassassin')
provides=('init-spamassassin')
source=("spamd")
sha256sums=('b53da898b1eb3b6ab49258efdc1f02a067e5697df94ec3a196557c88592b2987')

package() {
    install -Dm644 spamd "$pkgdir/etc/dinit.d/spamd"
}
