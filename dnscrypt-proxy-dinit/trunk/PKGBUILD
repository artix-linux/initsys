# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=dnscrypt-proxy-dinit
pkgver=20211025
pkgrel=2
pkgdesc="dinit service scripts for dnscrypt-proxy"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('dnscrypt-proxy' 'dinit')
groups=('dinit-galaxy')
conflicts=('init-dnscrypt-proxy')
provides=('init-dnscrypt-proxy')
source=("dnscrypt-proxy")
sha256sums=('37bfe8fe14dc4913155d494ba76f350ab2207a6cf1e0ada1a8e389fceb2554ef')

package() {
    install -Dm644 dnscrypt-proxy "$pkgdir/etc/dinit.d/dnscrypt-proxy"
}
