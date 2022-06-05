# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=bftpd-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for bftpd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('bftpd' 'dinit')
conflicts=('init-bftpd')
provides=('init-bftpd')
source=("bftpd")
sha256sums=('1bfc337147834f2290f7b5ecb923d7bd02b92c1badaa8a7800da929b308992a9')

package() {
    install -Dm644 bftpd "$pkgdir/etc/dinit.d/bftpd"
}
