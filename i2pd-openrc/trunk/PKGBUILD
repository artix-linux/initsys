# Maintainer linuxer <https://gitea.artixlinux.org/linuxer>

pkgname=i2pd-openrc
pkgdesc="i2pd OpenRC init script"
pkgver=20210505
pkgrel=1
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
groups=('openrc-galaxy')
license=('GPL2')
depends=('openrc' 'i2pd')
provides=('init-i2pd')
conflicts=('init-i2pd')
source=("i2pd.initd")
b2sums=('6ff6e7d3a8d159258350da731d6c19cda171474b2bee163dd12ebb78538ac1d97fdbb0ba3ea6b45df8c93c9eaacf77e825b135e53b23bf91b48bff74af318f12')

package() {
    install -Dm755 i2pd.initd "$pkgdir/etc/init.d/i2pd"
}
