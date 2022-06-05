# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=apparmor-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service script for AppArmor"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
provides=('init-apparmor')
conflicts=('init-apparmor')
depends=('apparmor' 'dinit')
source=('apparmor')
sha256sums=('8a66c3569ce5be36eec52af60e24402d689b50a53ad7b0dd29f2becef02a4e48')

package() {
    install -Dm644 apparmor "${pkgdir}/etc/dinit.d/apparmor"
}
