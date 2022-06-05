# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=lvm2-s6
pkgver=20220124
pkgrel=1
pkgdesc="s6-rc service scripts for lvm2"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-system')
provides=('init-lvm2')
conflicts=('init-lvm2')
depends=('lvm2' 's6-base')
makedepends=('git')
backup=('etc/s6/config/lvm2.conf')
_commit=394046cbe4323e981a27cb0f6afe2e3427f1ca11
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "lvm2" "${pkgdir}"
}
