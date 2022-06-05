# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=fcgiwrap-dinit
pkgver=20220424
pkgrel=1
pkgdesc="dinit service scripts for fcgiwrap"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('fcgiwrap' 'dinit')
conflicts=('init-fcgiwrap')
provides=('init-fcgiwrap')
source=("fcgiwrap")
sha256sums=('fbcfbd8ce3b60d6a73870a359587fb7195f8bbc0dda9d537ecdd6c7c8ac5b0c3')

package() {
    install -Dm644 fcgiwrap "$pkgdir/etc/dinit.d/fcgiwrap"
}
