# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=coturn-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc//} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'coturn')
provides=('init-coturn')
conflicts=('init-coturn')
source=("coturn.initd")
md5sums=('e22f6e5c58eb37ce0246d91367163241')

package() {
	install -Dm755 "$srcdir/coturn.initd" "$pkgdir/etc/init.d/coturn"
}
