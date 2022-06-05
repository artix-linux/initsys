# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=strongswan-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc//} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/PackagesS/strongswan-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'strongswan')
provides=('init-strongswan')
conflicts=('init-strongswan')
source=("strongswan.initd"
	"charon.initd")
md5sums=('9c0557cbd2caff7262e9ad31d904aa14'
         '48a259254c4a3fd110aab60542703f2f')

_inst_initd(){
   install -Dm755 ${srcdir}/charon.initd ${pkgdir}/etc/init.d/charon
   install -Dm755 ${srcdir}/strongswan.initd ${pkgdir}/etc/init.d/strongswan
}

package() {
    _inst_initd "${pkgname/-openrc/}"
}
