# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
# Contributor: artoo <artoo@artixlinux.org> 
pkgname=s6-base
pkgver=2.6.1
pkgrel=1
pkgdesc='Packages, hooks, and scripts to define a basic s6 init system implementation for Artix Linux.'
url='https://gitea.artixlinux.org/artix/alpm-hooks'
arch=('any')
license=('GPL')
depends=('s6-contrib' 's6-linux-init')
makedepends=('git')
provides=('svc-manager' 'init-rc')
conflicts=('svc-manager' 'init-rc')
backup=('etc/s6/config/s6-rc-db-update.conf')
_commit=57bcc7fee22d75df96fd546ee7215166cdfb1233
source=("git+https://gitea.artixlinux.org/artix/alpm-hooks.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/alpm-hooks
    DESTDIR="${pkgdir}" make install_s6
    install -v -d "${pkgdir}"/etc/s6/rc
}
