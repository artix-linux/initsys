# Maintainer: Dudemanguy <dudemanguy@artixlinux.org> 
pkgname=v2ray-s6
pkgver=20220927
pkgrel=1
pkgdesc="s6-rc service scripts for v2ray"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-galaxy')
provides=('init-v2ray')
conflicts=('init-v2ray')
depends=('v2ray' 's6-base')
makedepends=('git')
_commit=f825fe17f9b24edca05a6c9cae5083fbb14acada
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "v2ray" "${pkgdir}"
}
