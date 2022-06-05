# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=opensmtpd-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'opensmtpd')
provides=('init-opensmtpd')
conflicts=('init-opensmtpd')
source=("${pkgname/-openrc/}.initd")
b2sums=('2b08eae5ccfc3578c495c18baa336892441b5bcea2b4a97597298efa685768d3377c5180c082329649acb14f47b4fc085cb6b1b43b6c00b57309743e626867f9')

package() {
	install -Dm755 "$srcdir/opensmtpd.initd" "$pkgdir/etc/init.d/opensmtpd"
}
