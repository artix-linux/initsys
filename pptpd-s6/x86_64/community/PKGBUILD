# Maintainer: Dudemanguy <dudemanguy@artixlinux.org> 
# Contributor: Nathan Owens <ndowens@artixlinux.org> 
pkgname=pptpd-s6
pkgver=20210919
pkgrel=1
pkgdesc="s6-rc service scripts for pptpd"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-world')
provides=('init-pptpd')
conflicts=('init-pptpd')
depends=('pptpd' 's6-base')
makedepends=('git')
_commit=f8db772e97393417271f286a3c9dc136d25a959c
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "pptpd" "${pkgdir}"
}
