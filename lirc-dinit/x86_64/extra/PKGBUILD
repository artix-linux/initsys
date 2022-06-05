# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=lirc-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for lirc"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('lirc' 'dinit')
conflicts=('init-lirc')
provides=('init-lirc')
source=("lircd")
sha256sums=('edf9c10a7497a994e0f88990d92b2d7e1064397b29c00ad0bce9fd9997b727cc')

package() {
    install -Dm644 lircd "$pkgdir/etc/dinit.d/lircd"
}
