# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=rpcbind-s6
pkgver=20210919
pkgrel=1
pkgdesc="s6 service scripts for rpcbind"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-system')
provides=('init-rpcbind')
conflicts=('init-rpcbind')
depends=('rpcbind' 's6-base')
makedepends=('git')
backup=('etc/s6/config/rpcbind.conf')
_commit=f8db772e97393417271f286a3c9dc136d25a959c
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "rpcbind" "${pkgdir}"
}
