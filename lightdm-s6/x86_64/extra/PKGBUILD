# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=lightdm-s6
pkgver=20220410
pkgrel=1
pkgdesc="s6-rc service scripts for lightdm"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-world')
provides=('init-lightdm')
conflicts=('init-lightdm')
depends=('lightdm' 'logind-s6' 's6-base')
makedepends=('git')
backup=('etc/s6/config/lightdm.conf')
_commit=7813296e9da1e936752e16daf12492b0a49b4527
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "lightdm" "${pkgdir}"
}
