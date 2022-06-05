# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=dns-over-https-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'dns-over-https')
provides=('init-dns-over-https')
conflicts=('init-dns-over-https')
source=("doh-server.initd"
	"doh-client.initd")
sha256sums=('fdbf2a6ac4e441eb6c6780cf0aab8a3d3621a03b0b71ca04b68763d6da520019'
            '6f9bc55be0b770ab15320393677ba9fb2c4f09df62c4f0af2e557907cb0ec484')

package() {
    install -Dm755 ${srcdir}/doh-server.initd ${pkgdir}/etc/init.d/doh-server
    install -Dm755 ${srcdir}/doh-client.initd ${pkgdir}/etc/init.d/doh-client
}
