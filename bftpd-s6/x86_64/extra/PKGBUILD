# Maintainer: Dudemanguy <dudemanguy@artixlinux.org> 
# Contributer: Nathan Owens <ndowens@artixlinux.org> 
pkgname=bftpd-s6
pkgver=20210919
pkgrel=1
pkgdesc="s6-rc service scripts for bftpd"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-world')
provides=('init-bftpd')
conflicts=('init-bftpd')
depends=('bftpd' 's6-rc')
makedepends=('git')
_commit=f8db772e97393417271f286a3c9dc136d25a959c
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "bftpd" "${pkgdir}"
}
