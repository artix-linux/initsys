# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=cryptsetup-s6
pkgver=20220124
pkgrel=1
pkgdesc="s6-rc service scripts for cryptsetup"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-system')
provides=('init-cryptsetup')
conflicts=('init-cryptsetup')
depends=('cryptsetup' 's6-base')
makedepends=('git')
_commit=394046cbe4323e981a27cb0f6afe2e3427f1ca11
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "cryptsetup" "${pkgdir}"
}
