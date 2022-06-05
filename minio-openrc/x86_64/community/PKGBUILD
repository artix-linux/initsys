# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=minio-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="http://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'minio')
provides=('init-minio')
conflicts=('init-minio')
backup=("etc/conf.d/${pkgname/-openrc/}")
source=("${pkgname/-openrc/}.initd"
	"${pkgname/-openrc/}.confd")
md5sums=('a193f4481c67f0871c77cab9d30bd4bd'
         '6ec61a82eaad9eeb0869f7770c12b75e')

package() {
	install -Dm755 "$srcdir/minio.initd" "$pkgdir/etc/init.d/minio"
	install -Dm644 "$srcdir/minio.confd" "$pkgdir/etc/conf.d/minio"
}
