# Maintainer: Qontinuum <qontinuum@artixlinux.org>
# Contributor: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=seatd-runit
pkgver=20220828
pkgrel=1
pkgdesc='runit service script for seatd'
arch=(any)
url='https://artixlinux.org'
license=(BSD)
depends=(dbus-runit seatd)
provides=(init-logind)
conflicts=(init-logind init-elogind)
install=seatd.install
source=(seatd.run seatd.check)
sha256sums=(dc9be620e32933e1adaa3b3074da65f5b0370e5deaeb32a5b80cddcd684926ee
            75736610d5253b82c6901fe47c224f698c40b56015e8e1ad09b88d3ad576c8f1)

package() {
    cd "$srcdir"
    install -Dm755 seatd.run "$pkgdir/etc/runit/sv/seatd/run"
    install -Dm755 seatd.check "$pkgdir/etc/runit/sv/seatd/check"

    install -d "${pkgdir}/etc/runit/runsvdir/default"
    ln -s seatd "${pkgdir}/etc/runit/sv/logind"
    ln -s ../../sv/logind "${pkgdir}/etc/runit/runsvdir/default/logind"
}
