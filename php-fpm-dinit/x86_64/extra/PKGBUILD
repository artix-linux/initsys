# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=php-fpm-dinit
pkgver=20211025
pkgrel=2
pkgdesc="dinit service scripts for php-fpm"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('php-fpm' 'dinit')
conflicts=('init-php-fpm')
provides=('init-php-fpm')
source=("php-fpm")
sha256sums=('f9758f5ffb88ef269615b25dd2190b61ab67b21f36ad7a0efef328c27083c528')

package() {
    install -Dm644 php-fpm "$pkgdir/etc/dinit.d/php-fpm"
}
