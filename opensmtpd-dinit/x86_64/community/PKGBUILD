# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=opensmtpd-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for opensmtpd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('opensmtpd' 'dinit')
conflicts=('init-opensmtpd')
provides=('init-opensmtpd')
source=("smtpd")
sha256sums=('24d97d523b73fcc4c43cad96b5f023a8fb98de089f30d1eedff69bef325ee37f')

package() {
    install -Dm644 smtpd "$pkgdir/etc/dinit.d/smtpd"
}
