# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=ntp-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for ntp"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('ntp' 'dinit')
conflicts=('init-ntp' 'init-timed' 'openntpd-dinit')
provides=('init-ntp' 'init-timed')
source=("ntpd")
sha256sums=('499905e4256c39c850d2278acbb674a2ff70de12ec6332afdecedf180b679603')

package() {
    install -Dm644 ntpd "$pkgdir/etc/dinit.d/ntpd"
}
