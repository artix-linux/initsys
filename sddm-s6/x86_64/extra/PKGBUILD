# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=sddm-s6
pkgver=20230210
pkgrel=1
pkgdesc="s6-rc service scripts for sddm"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-world')
provides=('init-sddm')
conflicts=('init-sddm')
depends=('sddm' 'logind-s6' 's6-base')
makedepends=('git')
_commit=be1d112f9b02073d9811e2abad17c3e91876c787
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "sddm" "${pkgdir}"
}
