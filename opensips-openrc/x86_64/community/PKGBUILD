# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=opensips-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'opensips')
provides=('init-opensips')
conflicts=('init-opensips')
backup=("etc/conf.d/${pkgname/-openrc/}")
source=("${pkgname/-openrc/}.confd"
	    "${pkgname/-openrc/}.initd")
b2sums=('d264df7ecbc9aaa4e1b2da2bc270f365ca8b5266791b9ff93d683b5d6892c1a9bfccfcdf10973095d4f2803dad3003095f0a56fa243c6815ca1c8d86407846af'
        '9b2792ae79b42262611f4f5d3be5cbafa3940d30ebc5b7554b9c2661590747210979e3735d60f9dc9fba2f011eea2a614b01afa93f58e74119a41cf170f44178')

package() {
	install -Dm755 "$srcdir/opensips.initd" "$pkgdir/etc/init.d/opensips"
	install -Dm644 "$srcdir/opensips.confd" "$pkgdir/etc/conf.d/opensips"
}
