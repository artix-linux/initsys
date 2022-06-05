# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=networkmanager-s6
pkgver=20220523
pkgrel=1
pkgdesc="s6-rc service scripts for networkmanager"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-world')
provides=('init-networkmanager')
conflicts=('init-networkmanager')
depends=('networkmanager' 'logind-s6' 's6-base')
makedepends=('git')
backup=('etc/s6/config/networkmanager.conf')
_commit=ee58a63b42eab89f666b8d609bedd2e9cb488a46
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "networkmanager" "${pkgdir}"
}
