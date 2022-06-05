# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=power-profiles-daemon-s6
pkgver=20220512
pkgrel=1
pkgdesc="s6-rc service scripts for power-profiles-daemon"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-world')
provides=('init-power-profiles-daemon')
conflicts=('init-power-profiles-daemon')
depends=('power-profiles-daemon' 'dbus-s6' 's6-base')
makedepends=('git')
backup=('etc/s6/config/power-profiles-daemon.conf')
_commit=17f4bd111b98ea8173dff170f95a0451677abfde
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "power-profiles-daemon" "${pkgdir}"
}
