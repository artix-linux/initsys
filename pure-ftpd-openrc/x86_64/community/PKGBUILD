# Maintainer: artoo <artoo@artixlinux.org>

pkgname=pure-ftpd-openrc
pkgver=20211104
pkgrel=1
pkgdesc="OpenRC pure-ftpd init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('init-pure-ftpd')
depends=('openrc' 'pure-ftpd')
conflicts=('init-pure-ftpd')
backup=('etc/conf.d/pure-ftpd')
source=("pure-ftpd".{confd,initd})
sha256sums=('a8aad401c412ade0aed9ba0974b60cf86aaf9357f7cdfd7d2e1ab22302396284'
            '4458ff145a1459b70d85557699aa879a47b8d87c2de9cff4fa6f00d5e2d04439')

package() {
    install -Dm755 "${srcdir}/pure-ftpd.initd" "${pkgdir}/etc/init.d/pure-ftpd"
    install -Dm644 "${srcdir}/pure-ftpd.confd" "${pkgdir}/etc/conf.d/pure-ftpd"
}
