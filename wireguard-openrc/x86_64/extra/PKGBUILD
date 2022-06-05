# Maintainer: Nathan Owens <ndowen@artixlinux.org>

pkgname=wireguard-openrc
pkgver=20210505
pkgrel=2
pkgdesc="OpenRC wireguard init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-wireguard')
depends=('openrc' 'wireguard-tools' 'resolvconf')
conflicts=('init-wireguard')
backup=(etc/conf.d/wireguard)
source=("wireguard."{initd,confd})
sha256sums=('62d437ef0c3409b73ef01329ea3265c690a272f1221c9119e3c7a881c2d26bcd'
            'ef2a35db4aeb29a1f2533fedc3b3208ca17cd6c32315a453df55d46e4927b61a')

package() {
    install -Dm755 "$srcdir"/wireguard.initd "$pkgdir"/etc/init.d/wireguard
    install -Dm644 "$srcdir"/wireguard.confd "$pkgdir"/etc/conf.d/wireguard
}
