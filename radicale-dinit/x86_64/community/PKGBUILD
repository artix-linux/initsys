# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=radicale-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for radicale"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('radicale' 'dinit')
conflicts=('init-radicale')
provides=('init-radicale')
source=("radicale")
sha256sums=('8fd5912cbf167469aa29d04334dd71508afc100752a6e7baba57a533bfb79350')

package() {
    install -Dm644 radicale "$pkgdir/etc/dinit.d/radicale"
}
