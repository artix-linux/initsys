# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=sslh-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC sslh init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'sslh')
provides=('init-sslh')
conflicts=('init-sslh')
backup=('etc/conf.d/sslh')
source=("sslh."{confd,initd})
sha256sums=('a4437487e4adf9463280384e8b83d52ac82ea3909c03ce1cf214008e680ca1c0'
            '70c03d5aa4498e757561af2394fe09f4927e5b336889ebac63729a441666ec20')

package() {
  install -Dm755 "$srcdir/sslh.initd" "$pkgdir/etc/init.d/sslh"
  install -Dm644 "$srcdir/sslh.confd" "$pkgdir/etc/conf.d/sslh"
}
