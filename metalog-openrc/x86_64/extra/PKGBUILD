# Maintainer: artoo <artoo@artixlinux.org>

pkgname=metalog-openrc
pkgver=20210505
pkgrel=2
pkgdesc="OpenRC metalog init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-metalog')
depends=('openrc' 'metalog')
conflicts=('init-metalog')
backup=('etc/conf.d/metalog')
source=("metalog.confd"
        "metalog.initd")
sha256sums=('dd9d30a6c22dca6d072a9c63e1494d3d0a26709a5f045ce5985642933fe24efc'
            '70d354651aaa7683afc98181b596009fc562c90cc6b6f9d3afd68c58fcf47402')

package() {
    install -Dm755 "${srcdir}"/metalog.initd "${pkgdir}"/etc/init.d/metalog
    install -Dm644 "${srcdir}"/metalog.confd "${pkgdir}"/etc/conf.d/metalog
}
