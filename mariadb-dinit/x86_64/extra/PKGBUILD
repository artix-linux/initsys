# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=mariadb-dinit
pkgver=20211026
pkgrel=2
pkgdesc="dinit service script for mariadb"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('mariadb' 'dinit')
groups=('dinit-world')
conflicts=('init-mariadb' 'init-mysql')
provides=('init-mariadb')
source=("mysqld" "mysqld.script")
sha256sums=('ff310c3d495e47d90805581518c079819f869f781d2068076cf40c55faa478c2'
            'd41cb14f7aceef6b233f58ff268e62b95676693d3a31df93b7af7dccdf4c7bda')

package() {
    install -Dm644 mysqld        "$pkgdir/etc/dinit.d/mysqld"
    install -Dm755 mysqld.script "$pkgdir/etc/dinit.d/scripts/mysqld"
}
