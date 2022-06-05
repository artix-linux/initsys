# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=apcupsd-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service script for apcupsd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('apcupsd' 'dinit')
groups=('dinit-galaxy')
provides=('init-apcupsd')
conflicts=('init-apcupsd')
source=("apcupsd")
sha256sums=('46cb064315aa71337f64127b90b03815129e8c7c283435ca001aa994b2fc10f6')

package() {
    install -Dm644 apcupsd "$pkgdir/etc/dinit.d/apcupsd"
}
