# Maintainer: artoo <artoo@artixlinux.org>

pkgname=lighttpd-openrc
pkgver=20210505
pkgrel=2
pkgdesc="OpenRC lighttpd init script"
arch=('any')
url="https://gitea.artixlinux.org/PackagesL/lighttpd-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-lighttpd')
depends=('openrc' 'lighttpd')
conflicts=('init-lighttpd')
backup=('etc/conf.d/lighttpd')
source=('lighttpd.confd'
        'lighttpd.initd')
sha256sums=('0be7c9c04ce508cbefb3e913951d83c5ed7f0e01fe5aebcf3a5071f30ef3dbc2'
            'e0a1c19fdda0254d37d9298d0b87f5b04c169d42584d657c2987ed3c41fab3d5')

package() {
    install -Dm644 "${srcdir}"/lighttpd.confd "${pkgdir}"/etc/conf.d/lighttpd
    install -Dm755 "${srcdir}"/lighttpd.initd "${pkgdir}"/etc/init.d/lighttpd
}
