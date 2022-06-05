# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=prometheus-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service script for prometheus"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('prometheus' 'dinit')
groups=('dinit-world')
conflicts=('init-prometheus')
provides=('init-prometheus')
source=("prometheus")
sha256sums=('f3095803c43d2430d74c9198ee7ac55975f23fe18e9180c4bdb97bec14ed470c')

package() {
    install -Dm644 prometheus "$pkgdir/etc/dinit.d/prometheus"
}
