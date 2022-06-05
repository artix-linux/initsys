# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=exim-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/PackagesE/exim-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'exim')
provides=('init-exim')
conflicts=('init-exim')
backup=("etc/conf.d/${pkgname/-openrc/}")
source=("exim.confd"
	    "exim.initd")
sha256sums=('db711754c48dfb7e3810009a1c6ffa331625c9d74d00dc8fa8256d9fa2c353f0'
            'fac5a60e64f5e04e19ef65029bc3064af26626b8986f91356d305630714340e3')

package() {
  install -Dm644 "$srcdir"/exim.confd "$pkgdir"/etc/conf.d/exim
  install -Dm755 "$srcdir"/exim.initd "$pkgdir"/etc/init.d/exim
}
