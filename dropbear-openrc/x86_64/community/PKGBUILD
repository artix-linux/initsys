# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=dropbear-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'dropbear')
provides=('init-dropbear')
conflicts=('init-dropbear')
backup=("etc/conf.d/${pkgname/-openrc/}")
source=("${pkgname/-openrc/}.initd"
	"${pkgname/-openrc/}.confd")
sha256sums=('38bc266fb5b1e55f710c0c349fde677c0cb9d313eb76bd84d87a68515f459f44'
            'e891255a49d408eb11514662faa4d724a1df27cc2ee90268507dbd2573b67334')

package() {
	install -Dm755 "$srcdir/dropbear.initd" "$pkgdir/etc/init.d/dropbear"
	install -Dm644 "$srcdir/dropbear.confd" "$pkgdir/etc/conf.d/dropbear"
}
