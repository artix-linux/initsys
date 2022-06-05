# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
# Contributor: Nathan <ndowens@artixlinux.org>
pkgname=fcron-s6
pkgver=20210919
pkgrel=1
pkgdesc="s6-rc service scripts for fcron"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-galaxy')
provides=('init-fcron' 'init-cron')
conflicts=('init-fcron' 'init-cron')
depends=('fcron' 's6-base')
makedepends=('git')
backup=('etc/s6/config/fcron.conf')
_commit=f8db772e97393417271f286a3c9dc136d25a959c
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "fcron" "${pkgdir}"
}
