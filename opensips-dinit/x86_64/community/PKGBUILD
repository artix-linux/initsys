# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=opensips-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for opensips"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('opensips' 'dinit')
conflicts=('init-opensips')
provides=('init-opensips')
source=("opensips")
sha256sums=('327409f1615e6dfc98caa7865f87cbdcced0ec2e9a11d681639c070044a5eed6')

package() {
    install -Dm644 opensips "$pkgdir/etc/dinit.d/opensips"
}
