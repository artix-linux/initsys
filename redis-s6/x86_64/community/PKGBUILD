# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
# Contributor: Nathan Owens <ndowens@artixlinux.org>
pkgname=redis-s6
pkgver=20230429
pkgrel=1
pkgdesc="s6-rc service scripts for redis"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-galaxy')
provides=('init-redis')
conflicts=('init-redis')
depends=('redis' 's6-base')
makedepends=('git')
backup=('etc/s6/config/redis.conf')
_commit=5d699023ba6c2fc0a5b687c725dc0206ae4ee1fa
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "redis" "${pkgdir}"
}
