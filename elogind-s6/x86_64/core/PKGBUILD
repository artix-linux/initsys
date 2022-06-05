# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=elogind-s6
pkgver=20220123
pkgrel=1
pkgdesc="s6-rc service scripts for elogind"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
depends=('elogind' 'dbus-s6' 's6-base')
makedepends=('git')
provides=('logind-s6' 'init-logind' 'init-elogind')
conflicts=('logind-s6' 'init-logind' 'init-elogind')
_commit=2fff2bc2c20464f1641c4b7077d3db4a67fff3f4
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "elogind" "${pkgdir}"
}
