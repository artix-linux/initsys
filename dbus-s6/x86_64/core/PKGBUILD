# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=dbus-s6
pkgver=20210918
pkgrel=1
pkgdesc="s6-rc service scripts for dbus"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-system')
depends=('dbus' 's6-base')
makedepends=('git')
provides=('init-dbus')
conflicts=('init-dbus')
backup=('etc/s6/config/dbus.conf')
_commit=f8db772e97393417271f286a3c9dc136d25a959c
_hook_commit=0bb100c62bbde2878a242cc72626d00462c921b5
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit"
        "git+https://gitea.artixlinux.org/artix/alpm-hooks.git#commit=$_hook_commit")
sha256sums=('SKIP'
            'SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "dbus" "${pkgdir}"

    cd "${srcdir}"/alpm-hooks
    make DESTDIR="${pkgdir}" install_s6_dbus
}
