# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
# Contributor: Nathan <ndowens@artixlinux.org>
pkgname=docker-s6
pkgver=20230512
pkgrel=1
pkgdesc="s6-rc service scripts for docker"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-galaxy')
provides=('init-docker')
conflicts=('init-docker')
depends=('containerd-s6' 'docker' 's6-base')
makedepends=('git')
backup=('etc/s6/config/docker.conf')
_commit=93d1cd4a3aa8c2d6800a81d433e5c606256afe33
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "docker" "${pkgdir}"
}
