# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=samba-s6
pkgver=20211002
pkgrel=1
pkgdesc="s6-rc service scripts for samba"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-world')
provides=('init-samba')
conflicts=('init-samba')
depends=('samba' 's6-base')
makedepends=('git')
backup=('etc/s6/config/samba.conf')
_commit=9e6e7066e21259da3bf92f6bc83fd78c9e5db8e0
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "samba" "${pkgdir}"
}
