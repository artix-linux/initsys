# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=ddclient-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC ddclient init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'ddclient')
provides=('init-ddclient')
conflicts=('init-ddclient')
source=("ddclient.initd")
sha256sums=('61aad153a4ca385089eefb6f03190c0e2629e2f674278e426a34a746f5524695')

package() {
    install -Dm755 "${srcdir}/ddclient.initd" "${pkgdir}/etc/init.d/ddclient"
}
