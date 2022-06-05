# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
# Contributor: Nathan <ndowens@artixlinux.org>
pkgname=php-fpm-s6
pkgver=20210919
pkgrel=1
pkgdesc="s6-rc service scripts for php-fpm"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-world')
provides=('init-php-fpm')
conflicts=('init-php-fpm')
depends=('php-fpm' 's6-base')
makedepends=('git')
backup=('etc/s6/config/php-fpm.conf')
_commit=f8db772e97393417271f286a3c9dc136d25a959c
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "php-fpm" "${pkgdir}"
}
