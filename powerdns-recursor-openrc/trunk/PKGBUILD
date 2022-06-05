# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=powerdns-recursor-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'powerdns-recursor')
provides=('init-powerdns-recursor')
conflicts=('init-powerdns-recursor')
source=("pdns-recursor.initd")
b2sums=('4fe41e467978a0c5d8a260e7fd718ccbbcfa0e4193bec8694683a51f22105aeb335d909ec7419461c063989d6b57a1f89b229abe8eaafbad2b440ca2bd83fe5e')

package() {
    install -Dm755 ${srcdir}/pdns-recursor.initd ${pkgdir}/etc/init.d/pdns-recursor
}
