# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=mopidy-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="http://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'mopidy')
provides=('init-mopidy')
conflicts=('init-mopidy')
backup=('etc/conf.d/mopidy')
source=("${pkgname/-openrc/}.initd"
	"${pkgname/-openrc/}.confd")
md5sums=('14899a5cede1bb8ed653ac8f17d262ae'
         '4959277c789bdffd8fa296fe5a7dc8c9')

package() {
	install -Dm755 "$srcdir/mopidy.initd" "$pkgdir/etc/init.d/mopidy"
	install -Dm644 "$srcdir/mopidy.confd" "$pkgdir/etc/conf.d/mopidy"
}
