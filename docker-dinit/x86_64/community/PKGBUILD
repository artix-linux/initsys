# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=docker-dinit
pkgver=20211025
pkgrel=2
pkgdesc="dinit service script for docker"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('docker' 'dinit')
groups=('dinit-galaxy')
provides=('init-docker')
conflicts=('init-docker')
source=("dockerd" "dockerd.script")
sha256sums=('6dc7d42f628a70b8fbae3b5fcad65514fa54233279c03648961d8a2cba82c2e8'
            '7fcda58e7782fe7a846275aa26cdc0d76291f035789023774f33ced2e97021aa')

package() {
    install -Dm644 dockerd        "$pkgdir/etc/dinit.d/dockerd"
    install -Dm755 dockerd.script "$pkgdir/etc/dinit.d/scripts/dockerd"
}
