# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=fcgiwrap-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'fcgiwrap')
provides=('init-fcgiwrap')
conflicts=('init-fcgiwrap')
backup=("etc/conf.d/${pkgname/-openrc/}")
source=("${pkgname/-openrc/}."{initd,confd})
sha256sums=('99db01d25c39d0a0f7de679eef25fe6504d2d9c6322d7cd88b4a4508b7e7a0f1'
            '22bf354841c0486bdf5e7909adc47092690fb09520841f8aa2f11ef4e0ee651d')

package() {
  install -Dm755 "$srcdir/fcgiwrap.initd" "$pkgdir/etc/init.d/fcgiwrap"
  install -Dm644 "$srcdir/fcgiwrap.confd" "$pkgdir/etc/conf.d/fcgiwrap"
}
