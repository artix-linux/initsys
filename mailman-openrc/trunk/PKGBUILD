# Maintainer: artoo <artoo@artixlinux.org>

pkgname=mailman-openrc
pkgver=20210210
pkgrel=1
pkgdesc="OpenRC mailman init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('init-mailman')
depends=('openrc' 'mailman')
conflicts=('init-mailman')
source=("mailman.initd")
sha256sums=('870d52074566fd25dda39dc424b3f33122dbe7bd609c891f70c91ee67344dc82')

package() {
    install -Dm755 "${srcdir}"/mailman.initd "${pkgdir}"/etc/init.d/mailman
}


