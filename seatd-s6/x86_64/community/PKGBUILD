# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=seatd-s6
pkgver=20220605
pkgrel=1
pkgdesc="s6-rc service scripts for seatd"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
depends=('seatd' 's6-base')
makedepends=('git')
provides=('logind-s6' 'init-logind' 'init-seatd')
conflicts=('logind-s6' 'init-logind' 'init-seatd')
_commit=3d527155254bb338279b27cb7f47745266d95a14
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "seatd" "${pkgdir}"
}
