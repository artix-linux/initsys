# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=tinydns-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'tinydns')
provides=('init-tinydns')
conflicts=('init-tinydns')
source=("${pkgname/-openrc/}.initd")
md5sums=('6404299870581a8a019c8020478af81f')

package() {
  install -Dm755 "$srcdir/tinydns.initd" "$pkgdir/etc/init.d/tinydns"
}
