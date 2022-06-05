# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=at-openrc
pkgver=20210506
pkgrel=2
pkgdesc="OpenRC at init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('init-atd')
depends=('openrc' 'at')
conflicts=('init-atd')
backup=('etc/conf.d/atd')
source=(atd.{confd,initd}
        80-atd.hook)
sha256sums=('ab023e245103b6e0786ad1888143fdb87933ff5937114ac086f0616d6b620c02'
            'd0a18f3dc45e42074fa071e915a847a5bb84faa1365e5a667bafea607f178526'
            'f94ccf3dd594b98d1e46b9316f8db8b1a2500c8bc6a5a78ce957fb7070bbc698')

package() {
    install -Dm755 "${srcdir}/atd.initd" "${pkgdir}/etc/init.d/atd"
    install -Dm644 "${srcdir}/atd.confd" "${pkgdir}/etc/conf.d/atd"
    install -Dt "${pkgdir}"/usr/share/libalpm/hooks -m644 *.hook
}
