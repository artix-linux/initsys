# Maintainer: Nathan <ndowens@artixlinux.org>
# Maintainer: Artoo <artoos@artixlinux.org>

pkgname=veracrypt-openrc
pkgver=20211122
pkgrel=1
pkgdesc="OpenRC veracrypt init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('init-veracrypt')
depends=('openrc' 'veracrypt')
conflicts=('init-veracrypt')
source=("veracrypt.initd")
sha256sums=('9d36240b698b97d6384ea3d4b282b1765f301adb71c5e80e190aa0e985ca1e53')

package() {
    install -Dm755 "${srcdir}"/veracrypt.initd "${pkgdir}"/etc/init.d/veracrypt
}

