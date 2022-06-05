# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
# Contributor: Nathan <ndowens@artixlinux.org>
pkgname=brltty-s6
pkgver=20210919
pkgrel=1
pkgdesc="s6-rc service scripts for brltty"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-world')
provides=('init-brltty')
conflicts=('init-brltty')
depends=('brltty' 's6-base')
makedepends=('git')
backup=('etc/s6/config/brltty.conf')
_commit=f8db772e97393417271f286a3c9dc136d25a959c
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "brltty" "${pkgdir}"
}
