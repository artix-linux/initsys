# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=fcron-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for fcron"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('fcron' 'dinit')
conflicts=('init-fcron' 'init-cron')
provides=('init-fcron' 'init-cron')
source=("fcron")
sha256sums=('0fe925ff808e98bde301fb6361478168c572b19effc247294fcefdbbbce8bffb')

package() {
    install -Dm644 fcron "$pkgdir/etc/dinit.d/fcron"
}
