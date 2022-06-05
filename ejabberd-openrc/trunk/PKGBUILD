# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=ejabberd-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'ejabberd')
provides=('init-ejabberd')
conflicts=('init-ejabberd')
backup=("etc/conf.d/${pkgname/-openrc/}")
source=("ejabberd.confd"
	"ejabberd.initd")
sha256sums=('e866e279da009486f2072b33c38662be96032ab7845f28a8a7ca123f8e361c3b'
            'c80044ca345c8a82a920bc0e11b0ec548c63efb2bd3e240dde86a42809e2537f')

package() {
	install -Dm755 "$srcdir/ejabberd.initd" "$pkgdir/etc/init.d/ejabberd"
	install -Dm644 "$srcdir/ejabberd.confd" "$pkgdir/etc/conf.d/ejabberd"
}
