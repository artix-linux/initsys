# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=lxd-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'lxd')
provides=('init-lxd')
conflicts=('init-lxd')
backup=("etc/conf.d/${pkgname/-openrc/}")
source=("lxd.initd"
	    "lxd.confd")
sha256sums=('f3181ee5b163f588f7d4fecbe8b3717426edc13e8fdb585b8f9fa7e43a2ce9b9'
            'c8363079b0d78e59d845372f532058eee6243e203a5eae754a2b4bec08d44609')

package() {
	install -Dm755 "$srcdir/lxd.initd" "$pkgdir/etc/init.d/lxd"
	install -Dm644 "$srcdir/lxd.confd" "$pkgdir/etc/conf.d/lxd"
}
