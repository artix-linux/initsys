# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=vnstat-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for vnstat"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('vnstat' 'dinit')
conflicts=('init-vnstat')
provides=('init-vnstat')
source=("vnstatd")
sha256sums=('012064a046d42ffc5be6be9a635c868becc5ea5bfc71db0de6263047c6788019')

package() {
    install -Dm644 vnstatd "$pkgdir/etc/dinit.d/vnstatd"
}
