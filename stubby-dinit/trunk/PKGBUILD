# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=stubby-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for stubby"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('stubby' 'dinit')
conflicts=('init-stubby')
provides=('init-stubby')
source=("stubby")
sha256sums=('dce5e686e897836b4dab206a6aa30181bf6e24293f27601ed0cca856da86dd1d')

package() {
    install -Dm644 stubby "$pkgdir/etc/dinit.d/stubby"
}
