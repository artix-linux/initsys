# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=nsd-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'nsd')
provides=('init-nsd')
conflicts=('init-nsd')
source=("${pkgname/-openrc/}.initd")
b2sums=('140eb3b09656b1069165d2415970f6df5fca86d613f453be6d3fe3a1c1c6c3504a574d343dd4f5e253f13d1506f1b0d2d03657a982c22560cd5a8b0564460b89')

package() {
	install -Dm755 "$srcdir/nsd.initd" "$pkgdir/etc/init.d/nsd"
}
