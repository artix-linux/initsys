# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=rng-tools-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for rng-tools"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('rng-tools' 'dinit')
conflicts=('init-rng-tools')
provides=('init-rng-tools')
source=("rngd")
sha256sums=('8decccbc65e28e243ff45be0ebb6cb4d9aab15d0663479d0f737bfe5b451921a')

package() {
    install -Dm644 rngd "$pkgdir/etc/dinit.d/rngd"
}
