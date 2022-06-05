# Maintainer: Nathan Owens <ndowens@artixlinux.org>
# Contributer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=backuppc-s6
pkgver=20210919
pkgrel=1
pkgdesc="s6-rc service scripts for backuppc"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
license=('GPL2')
groups=('s6-galaxy')
provides=('init-backuppc')
conflicts=('init-backuppc')
depends=('s6-base' 'backuppc')
makedepends=('git')
_commit=f8db772e97393417271f286a3c9dc136d25a959c
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "backuppc" "${pkgdir}"
}
