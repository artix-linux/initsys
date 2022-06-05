# Maintainer: artoo <artoo@artixlinux.org>

pkgname=apache-openrc
pkgver=20210505
pkgrel=2
pkgdesc="OpenRC apache init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-apache')
depends=('apache' 'openrc')
conflicts=('init-apache')
backup=('etc/conf.d/httpd')
source=("httpd.initd"
	"httpd.confd")
sha256sums=('c3011deea0fe26fb7cf9a9b2b37b595e78227ba6baf2a0689c41dcfa52e32c42'
            'add98ad7786a5037828f61fb5e26072552eb3f9b1b0f77a5d67cc419020bb66e')

package() {
	install -Dm755 "${srcdir}"/httpd.initd "${pkgdir}"/etc/init.d/httpd
	install -Dm644 "${srcdir}"/httpd.confd "${pkgdir}"/etc/conf.d/httpd
}
