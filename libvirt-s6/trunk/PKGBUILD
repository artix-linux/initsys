# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=libvirt-s6
pkgver=20220503
pkgrel=1
pkgdesc="s6-rc service scripts for libvirt"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-galaxy')
provides=('init-libvirt')
conflicts=('init-libvirt')
depends=('libvirt' 'dbus-s6' 's6-base')
makedepends=('git')
_commit=f888ea7d81e22fac1350224daa558127d4d3b219
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "libvirt" "${pkgdir}"
}
