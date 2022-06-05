# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=transmission-openrc
pkgver=20210505
pkgrel=2
pkgdesc="OpenRC transmission init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-transmission')
depends=('openrc' 'transmission-cli')
conflicts=('init-transmission')
backup=("etc/conf.d/transmission")
source=("transmission".{confd,initd})
sha256sums=('a2d38989afc96788efa1dccf5dcfeb81278f8093e2c2a8c4129c9826aeaafd89'
            '9b435a7af81bf2904941ef1f165ec9621a4ba4a5d6aa6b823b36a11750ec89c8')
b2sums=('52cd64646a30ab09926c406022c819f75deb182b04006082d9aa49c91c129f31dd9c9e49456ddb23d746b87c7e157cb859eb09ef9dcd0a798d097469fcb5beba'
        '34ebb53495aa4339832fbf75f3ff515e15bd93329d0b6d88172589c9024b3b9a16a1c2436dabebb700687ca8d0f7115cd198a665bc51e7ca0b965bc2c929b999')

package() {
    install -Dm755 "$srcdir"/transmission.initd "$pkgdir"/etc/init.d/transmission
    install -Dm644 "$srcdir"/transmission.confd "$pkgdir"/etc/conf.d/transmission
}

