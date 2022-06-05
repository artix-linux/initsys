# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=wpa_supplicant-s6
pkgver=20220207
pkgrel=1
pkgdesc="s6-rc service scripts for wpa_supplicant"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-system')
provides=('init-wpa_supplicant')
conflicts=('init-wpa_supplicant')
depends=('wpa_supplicant' 'dhcpcd-s6' 's6-base')
makedepends=('git')
backup=('etc/s6/config/wpa_supplicant.conf')
_commit=2cf4da956796594d8eeb478ae05341a67518d4cf
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "wpa_supplicant" "${pkgdir}"
}
