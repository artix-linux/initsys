# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=dhcpcd-s6
pkgver=20220207
pkgrel=1
pkgdesc="s6-rc service scripts for dhcpcd"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-system')
provides=('init-dhcpcd')
conflicts=('init-dhcpcd')
depends=('dhcpcd' 's6-base')
makedepends=('git')
backup=('etc/s6/config/dhcpcd.conf')
_commit=90c6b26364bd11585c31d67fad91dbbb42383bc1
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "dhcpcd" "${pkgdir}"
}
