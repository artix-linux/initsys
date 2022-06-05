# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
# Maintainer: Artoo <artoo@artixlinux.org>

pkgname=s6-contrib
pkgver=1.0
pkgrel=1
pkgdesc='A collection of s6 convenience scripts.'
arch=('any')
url='https://gitea.artixlinux.org/artix/s6-contrib'
license=('GPL')
depends=('sh' 's6' 's6-scripts')
makedepends=('git')
backup=('etc/s6/s6-db-reload.conf')
_commit=1f3da8bf266e0bf95279e43d769b31437766c3c5 # git rev-parse $pkgver
source=("git+$url.git#commit=$_commit")
sha256sums=('SKIP')

build() {
    make -C "${pkgname}"
}

package() {
    make -C "${pkgname}" install DESTDIR="${pkgdir}"
}
