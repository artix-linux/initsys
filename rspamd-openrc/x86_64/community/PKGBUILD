# Maintainer: artoo <artoo@artixlinux.org>

pkgname=rspamd-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC rspamd init script"
arch=('any')
url="https://gitea.artixlinux.org/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'rspamd')
provides=('init-rspamd')
conflicts=('init-rspamd')
backup=('etc/conf.d/rspamd')
source=("rspamd.confd"
        "rspamd.initd")
sha256sums=('ef90d7b5002535b86f71c2676feffba744225c16ff8e826bf5048d87ede28305'
            '61bc5251d8453ac534bd1620c2baa06f8d24df72d9eb689ab7e8ac15b04a5ce0')

package() {
	install -Dm755 "${srcdir}"/rspamd.initd "${pkgdir}"/etc/init.d/rspamd
	install -Dm644 "${srcdir}"/rspamd.confd "${pkgdir}"/etc/conf.d/rspamd
}
