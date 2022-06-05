# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=matrix-synapse-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for matrix-synapse"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('matrix-synapse' 'dinit')
conflicts=('init-matrix-synapse')
provides=('init-matrix-synapse')
source=("matrix-synapse")
sha256sums=('1164c082ed6324682dbf4e8416ef0d1cf95f967671cd0fa50d8df876848007e7')

package() {
    install -Dm644 matrix-synapse "$pkgdir/etc/dinit.d/matrix-synapse"
}
