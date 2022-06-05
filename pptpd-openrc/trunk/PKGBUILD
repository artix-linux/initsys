# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=pptpd-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'pptpd')
provides=('init-pptpd')
conflicts=('init-pptpd')
backup=("etc/conf.d/${pkgname/-openrc/}")
source=("${pkgname/-openrc/}."{initd,confd})
sha256sums=('2d1fbfd5df2ac7b532ea76d15b7209ab238f4f524d75e1a397cf951fd0d4fc80'
            '4d69da546e36439dc1a7cb5abb949ad48046155752c047babb5472decdfa1958')

package() {
  install -Dm755 "$srcdir/pptpd.initd" "$pkgdir/etc/init.d/pptpd"
  install -Dm644 "$srcdir/pptpd.confd" "$pkgdir/etc/conf.d/pptpd"
}
