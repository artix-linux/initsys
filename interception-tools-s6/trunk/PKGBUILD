# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=interception-tools-s6
pkgver=20220123
pkgrel=1
pkgdesc="s6-rc service scripts for interception-tools"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-galaxy')
provides=('init-interception-tools')
conflicts=('init-interception-tools')
depends=('interception-tools' 's6-base')
makedepends=('git')
backup=('etc/s6/config/interception-tools.conf')
_commit=2fff2bc2c20464f1641c4b7077d3db4a67fff3f4
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "interception-tools" "${pkgdir}"
}
