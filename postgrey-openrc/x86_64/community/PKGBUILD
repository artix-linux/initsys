# Maintainer: nous@artixlinux.org
# Maintainer: artoo@artixlinux.org

pkgname=postgrey-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC postgrey init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'postgrey')
provides=('init-postgrey')
conflicts=('init-postgrey')
backup=('etc/conf.d/postgrey')
source=("postgrey.confd"
        "postgrey.initd")
sha256sums=('c4c5bfe68b99513152669443ee268186989a89f9846e7fd560841d4cb47fb031'
            'f4b3a47fd2550d6b36cf1e93f7452c98f06aff05b165a4e3cd6b9014ff2cbca5')

package() {
	install -Dm755 "$srcdir/postgrey.initd" "$pkgdir/etc/init.d/postgrey"
	install -Dm644 "$srcdir/postgrey.confd" "$pkgdir/etc/conf.d/postgrey"
}
