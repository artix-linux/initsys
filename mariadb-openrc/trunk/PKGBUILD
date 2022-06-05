# Maintainer: nous <nous@artixlinux.org>

pkgname=mariadb-openrc
pkgver=20210505
pkgrel=2
pkgdesc="OpenRC mariadb init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('mysql-openrc' 'init-mariadb')
depends=('mariadb' 'openrc')
conflicts=('init-mariadb')
replaces=('mysql-openrc')
source=('mariadb.initd' 'mariadb-supervise.initd')
sha256sums=('e047da01dcf47692f01daf0f37eba2e9669f459bba265bd75337f187f097e40c'
            'bb5281b04e7a8dd6048b8e7756969d683c6fa2231434615b540cf5310e63efb8')

package() {
    install -Dm755 "${srcdir}"/mariadb.initd "${pkgdir}"/etc/init.d/mariadb
    install -Dm755 "${srcdir}"/mariadb-supervise.initd "${pkgdir}"/etc/init.d/mariadb-supervise
}
