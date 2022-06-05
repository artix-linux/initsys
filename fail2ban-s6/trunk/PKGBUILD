# Maintainer: Nathan Owens <ndowens@artixlinux.org>
# Contributor: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=fail2ban-s6
pkgver=20210919
pkgrel=1
pkgdesc="s6-rc service scripts for fail2ban"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-galaxy')
provides=('init-fail2ban')
conflicts=('init-fail2ban')
depends=('fail2ban' 's6-base')
makedepends=('git')
backup=('etc/s6/config/fail2ban.conf')
_commit=f8db772e97393417271f286a3c9dc136d25a959c
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "fail2ban" "${pkgdir}"
}
