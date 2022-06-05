# Maintainer: artoo <artoo@artixlinux.org>

pkgname=fuse-openrc
pkgver=20210505
pkgrel=2
pkgdesc="OpenRC fuse init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-fuse')
depends=('openrc' 'fuse')
conflicts=('init-fuse')
source=("fuse.initd")
sha256sums=('294ac5f4d08cab106c42529cb10717a61a8b7158a1f429094f8543f13678ee9f')

package(){
	install -Dm755 "${srcdir}"/fuse.initd "${pkgdir}"/etc/init.d/fuse
}
