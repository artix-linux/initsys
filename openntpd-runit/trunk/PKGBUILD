# Maintainer: Qontinuum <qontinuum@artixlinux.org>
# Contributor: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=openntpd-runit
pkgver=20220306
pkgrel=1
pkgdesc='Runit service script for openntpd'
arch=('any')
url='https://artixlinux.org'
license=('BSD')
depends=('openntpd' 'runit')
groups=('runit-galaxy')
conflicts=('ntp' 'init-openntpd' 'init-timed')
provides=('init-timed')
install='openntpd-runit.install'
source=('openntpd.run'
        'openntpd.log.run')
b2sums=('58195e480ddacbddc19512d392e2403a9823479e2fd59736ca8a9637c0ef7550979b754091b7b8582b739dbbe6d9d830fc3271728c04ba1e2c52f4471455830c'
        '53fdf6906b6719445f8c976c6ffd62842a9f29dfcbc89ea1d5e60495e0fe45a814228e14dd4f71c6845df3652539b525495dbe1023a4275a4acd4270e7d9f2e0')

package() {
    cd "$srcdir"
    install -Dm755 openntpd.run "$pkgdir/etc/runit/sv/openntpd/run"
    install -Dm755 openntpd.log.run "$pkgdir/etc/runit/sv/openntpd/log/run"
}
