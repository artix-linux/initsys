# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=transmission-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for transmission"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('dinit' 'transmission-cli')
conflicts=('init-transmission')
provides=('init-transmission')
source=("transmission-daemon")
sha256sums=('ccbdfb5e584d016d1e41beb4eb98997bae9ec5afb9cfc1c7afd52f36c6f181e8')

package() {
    install -Dm644 transmission-daemon "$pkgdir/etc/dinit.d/transmission-daemon"
}
