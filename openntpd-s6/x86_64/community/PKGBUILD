# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=openntpd-s6
pkgver=20220306
pkgrel=1
pkgdesc="s6-rc service scripts for openntpd"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-galaxy')
provides=('init-openntpd' 'init-timed')
conflicts=('init-openntpd' 'init-timed')
depends=('openntpd' 's6-base')
makedepends=('git')
backup=('etc/s6/config/openntpd.conf')
_commit=faea983809f3b2c6a81273b6581344bc4ca8ac94
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "openntpd" "${pkgdir}"
}
