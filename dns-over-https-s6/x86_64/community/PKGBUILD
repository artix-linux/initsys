# Maintainer: Dudemanguy <dudemanguy@artixlinux.org> 
# Contributer: Nathan Owens <ndowens@artixlinux.org> 
pkgname=dns-over-https-s6
pkgver=20210919
pkgrel=1
pkgdesc="s6-rc service scripts for dns-over-https"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-galaxy')
provides=('init-dns-over-https')
conflicts=('init-dns-over-https')
depends=('dns-over-https' 's6-base')
makedepends=('git')
backup=('etc/s6/config/dns-over-https.conf')
_commit=f8db772e97393417271f286a3c9dc136d25a959c
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "dns-over-https" "${pkgdir}"
}
