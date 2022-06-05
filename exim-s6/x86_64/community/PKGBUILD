# Maintainer: Nathan <ndownes@artixlinux.org>
# Contributor: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=exim-s6
pkgver=20210919
pkgrel=1
pkgdesc="s6-rc service scripts for exim"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-galaxy')
provides=('init-exim')
conflicts=('init-exim')
depends=('exim' 's6-base')
makedepends=('git')
backup=('etc/s6/config/exim.conf')
_commit=f8db772e97393417271f286a3c9dc136d25a959c
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "exim" "${pkgdir}"
}
