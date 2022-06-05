# Maintainer: Nathan Owens <ndowens@artixlinux.org>
# Contributer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=opensips-s6
pkgver=20210919
pkgrel=1
pkgdesc="s6-rc service scripts for opensips"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-galaxy')
provides=('init-opensips')
conflicts=('init-opensips')
backup=('etc/s6/config/opensips.conf')
depends=('opensips' 's6-base')
makedepends=('git')
_commit=f8db772e97393417271f286a3c9dc136d25a959c
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "opensips" "${pkgdir}"
}
