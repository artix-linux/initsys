# Maintainer: Qontinuum <qontinuum@artixlinux.org>
# Contributor: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=docker-runit
pkgver=20220411
pkgrel=2
pkgdesc='Runit service script for docker'
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('docker' 'runit')
groups=('runit-galaxy')
provides=('init-docker')
conflicts=('init-docker')
install=docker-runit.install
source=('docker.run'
        'docker.log.run')
sha256sums=('b12f1fb958890063ff6e92ee653d0ac55ef4af97c3062736ab397444e9f7c13b'
            '8279f88223eaad7392ea0f7a567c7e432f4162c44752e8565b7ce109084ee069')

package() {
    cd "$srcdir"
    install -Dm755 docker.run "$pkgdir/etc/runit/sv/docker/run"
    install -Dm755 docker.log.run "$pkgdir/etc/runit/sv/docker/log/run"
}
