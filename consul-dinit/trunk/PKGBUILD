# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=consul-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for consul"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('consul' 'dinit')
conflicts=('init-consul')
provides=('init-consul')
source=("consul")
sha256sums=('d8227e1925204b7aa3f6b3eadeeb8e9f6d74a993a7ba6594af67bd6fd71c1f82')

package() {
    install -Dm644 consul "$pkgdir/etc/dinit.d/consul"
}
