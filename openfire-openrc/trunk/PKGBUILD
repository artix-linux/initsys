# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=openfire-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://codeberg.org/ndowens/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'openfire')
provides=('init-openfire')
conflicts=('init-openfire')
source=("${pkgname/-openrc/}.initd")
md5sums=('c4a52db8e28d6fc3aed6d25bbde28a76')

_inst_initd(){
    install -Dm755 ${srcdir}/$1.initd ${pkgdir}/etc/init.d/$1
}

package() {
    _inst_initd "${pkgname/-openrc/}"
}
