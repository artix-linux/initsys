# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
# Contributer: John Smith <promisedneverland@disroot.org>
pkgname=trojan-s6
pkgver=20210919
pkgrel=1
pkgdesc="s6-rc service scripts for trojan"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
license=(GPL)
groups=('s6-galaxy')
provides=('init-trojan')
conflicts=('init-trojan')
depends=('trojan' 's6-base')
makedepends=('git')
backup=('etc/s6/config/trojan.conf')
_commit=f8db772e97393417271f286a3c9dc136d25a959c
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "trojan" "${pkgdir}"
}
