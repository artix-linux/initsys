# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=alsa-utils-s6
pkgver=20220123
pkgrel=1
pkgdesc="s6-rc service scripts for alsa-utils"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-world')
provides=('init-alsa-utils')
conflicts=('init-alsa-utils')
depends=('alsa-utils' 's6-base')
makedepends=('git')
_commit=2fff2bc2c20464f1641c4b7077d3db4a67fff3f4
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "alsa-utils" "${pkgdir}"
}
