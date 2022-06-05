# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=shairplay-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'shairplay')
provides=('init-shairplay')
conflicts=('init-shairplay')
backup=("etc/conf.d/${pkgname/-openrc/}")
source=("${pkgname/-openrc/}."{initd,confd})
sha256sums=('9d965498d857d96b0399aac54c55673b7bc15dd4bf80303333cb3e3430338a4d'
            'b7a30e3b767858609e191c8937588e246a445a13744c51d1c6c447a2cb5d78a1')

package() {
  install -Dm755 "$srcdir/shairplay.initd" "$pkgdir/etc/init.d/shairplay"
  install -Dm644 "$srcdir/shairplay.confd" "$pkgdir/etc/conf.d/shairplay"
}
