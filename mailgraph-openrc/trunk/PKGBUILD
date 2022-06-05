# Maintainer: artoo <artoo@artixlinux.org>

pkgname=mailgraph-openrc
pkgver=20210419
pkgrel=1
pkgdesc="OpenRC mailgraph init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('init-mailgraph')
depends=('mailgraph' 'openrc')
conflicts=('init-mailgraph')
source=("mailgraph.confd"
        "mailgraph.initd")
sha256sums=('388f04177afbea00c2258a42377a530d3dc7272ff4319aab86536f687308f44a'
            'c35a416c6151bff2eddfbf24f9fdb59fdeed15df5ebca02ad45dad05115da834')

package() {
    install -Dm755 "${srcdir}"/mailgraph.confd "${pkgdir}"/etc/conf.d/mailgraph
    install -Dm755 "${srcdir}"/mailgraph.initd "${pkgdir}"/etc/init.d/mailgraph
}
