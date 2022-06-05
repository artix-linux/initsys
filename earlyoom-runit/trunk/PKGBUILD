# Maintainer: Muhammad Herdiansyah <konI@artixlinux.org>
# Contributor: linuxer <linuxer@artixlinux.org>

pkgname=earlyoom-runit
pkgver=20210405
pkgrel=1
url="https://artixlinux.org/"
pkgdesc="earlyoom runit service script"
arch=('x86_64')
license=('BSD')
depends=('earlyoom' 'runit')
source=("earlyoom.run")
sha256sums=('428034898eccbb624eb5c2e2084593d420a2ca548f9dd69f72ea3f9524808885')

package() {
    install -Dm755 ${srcdir}/earlyoom.run $pkgdir/etc/runit/sv/earlyoom/run
}
