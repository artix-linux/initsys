# Maintainer: Nathan Owens <ndowens@artixlinux.org>
# Maintainer: artoo <artoo@artixlinux.org>

pkgname=freeradius-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC freeradius init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'freeradius')
provides=('init-freeradius')
conflicts=('init-freeradius')
backup=('etc/conf.d/freeradiusd')
source=("freeradius.initd"
        "freeradius.confd")
sha256sums=('156e2e4ba8f92a903456a61bfcf4be765e7e2264e947399a9fd886f099f189af'
            '651f0e3a1ba4f3e201bb05546bc6faeff7ef3c8ba3529c9e75da87492a18aa5e')

package() {
	install -Dm755 "${srcdir}"/freeradius.initd "${pkgdir}"/etc/init.d/freeradiusd
	install -Dm644 "${srcdir}"/freeradius.confd "${pkgdir}"/etc/conf.d/freeradiusd
}
