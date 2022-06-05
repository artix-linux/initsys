# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
# Contributor: Nathan Owens <ndowens@artixlinux.org>
pkgname=rsync-s6
pkgver=20210919
pkgrel=1
pkgdesc="s6-rc service scripts for rsync"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-world')
provides=('init-rsync')
conflicts=('init-rsync')
depends=('rsync' 's6-base')
makedepends=('git')
backup=('etc/s6/config/rsync.conf')
_commit=f8db772e97393417271f286a3c9dc136d25a959c
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "rsync" "${pkgdir}"
}
