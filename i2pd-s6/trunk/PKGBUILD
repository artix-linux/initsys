# Maintainer: Dudemanguy <dudemanguy@artixlinux.org> 
pkgname=i2pd-s6
pkgver=20221202
pkgrel=1
pkgdesc="s6-rc service scripts for i2pd"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-galaxy')
provides=('init-i2pd')
conflicts=('init-i2pd')
depends=('i2pd' 's6-base')
makedepends=('git')
backup=('etc/s6/config/i2pd.conf')
_commit=2db7cb6f393b96711e636f98817ff40bc8f3f55d
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "i2pd" "${pkgdir}"
}
