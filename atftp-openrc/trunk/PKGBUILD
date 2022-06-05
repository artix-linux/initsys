# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=atftp-openrc
pkgver=20210506
pkgrel=1
pkgdesc="OpenRC script for atftp"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('init-atftp')
depends=('openrc' 'atftp')
conflicts=('init-atftp')
source=("atftp.initd")
sha256sums=('ca54e7b92db76df23cd82de921353ddd111f767ec06fafd252f43b93526a0b06')

package() {
	install -Dm755 "$srcdir/atftp.initd" "$pkgdir/etc/init.d/atftp"
}
