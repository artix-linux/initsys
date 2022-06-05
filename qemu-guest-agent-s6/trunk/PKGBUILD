# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=qemu-guest-agent-s6
pkgver=20210919
pkgrel=1
pkgdesc="s6-rc service scripts for qemu-guest-agent"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-world')
provides=('init-qemu-guest-agent')
conflicts=('init-qemu-guest-agent')
depends=('qemu-guest-agent' 's6-base')
makedepends=('git')
backup=('etc/s6/config/qemu-guest-agent.conf')
_commit=f8db772e97393417271f286a3c9dc136d25a959c
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "qemu-guest-agent" "${pkgdir}"
}
