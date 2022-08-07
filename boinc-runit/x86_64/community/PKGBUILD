# Maintainer: Q <qontinuum@artixlinux.org>
# Contributor: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=boinc-runit
pkgver=20220807
pkgrel=1
pkgdesc='Runit service script for boinc'
arch=('any')
url='https://artixlinux.org'
license=('BSD')
depends=('boinc' 'runit')
groups=('runit-galaxy')
provides=('init-boinc')
conflicts=('init-boinc')
backup=('etc/runit/sv/boinc/conf')
source=(boinc.run
        boinc.log.run
        boinc.conf)
sha256sums=('6faf5951862d0b93a86d4a9a191ea7112f7693093bfe5d6dbc36e66331493455'
            'c8183a22c8cb56d87157107d258cf93498dc7a341b155a442957b3ee64dd9726'
            '83b90c123205da8d4aadd3e761691bec25204109544e654f1d4cab659ed35537')

package() {
  cd "$srcdir"
  install -Dm755 boinc.run "$pkgdir/etc/runit/sv/boinc/run"
  install -Dm755 boinc.log.run "$pkgdir/etc/runit/sv/boinc/log/run"
  install -Dm644 boinc.conf "$pkgdir/etc/runit/sv/boinc/conf"
}
