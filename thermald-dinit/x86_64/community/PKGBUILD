# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=thermald-dinit
pkgver=20211103
pkgrel=1
pkgdesc="dinit service scripts for thermald"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('thermald' 'dinit')
conflicts=('init-thermald')
provides=('init-thermald')
source=("thermald")
sha256sums=('f67ed0e42fbbe93bb712f9c0608144529bd27c7744ea327ccdd31d3fd9713173')

package() {
    install -Dm644 thermald "$pkgdir/etc/dinit.d/thermald"
}
