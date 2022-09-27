# Maintainer: Nathan <ndowens@artixlinux.org>

pkgname=v2ray-openrc
pkgver=20220927
pkgrel=1
pkgdesc="OpenRC v2ray init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('init-v2ray')
depends=('openrc' 'v2ray')
conflicts=('init-v2ray')
source=("v2ray.initd")
sha256sums=('643a19c0daaf20605cb466cfba3c0af075b9854d1093edcdd7ba218284f14d11')

package() {
    install -Dm755 "${srcdir}"/v2ray.initd "${pkgdir}"/etc/init.d/v2ray
}

