# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>


pkgname=acpid-openrc
pkgver=20210506
pkgrel=1
pkgdesc="OpenRC acpid init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('init-acpid')
depends=('openrc' 'acpid')
conflicts=('init-acpid')
backup=('etc/conf.d/acpid')
source=("acpid.confd"
        "acpid.initd")
sha256sums=('3755d4eb8bb64a1304e5defedb949305ac550565da36fe4f94d5f31beee821ba'
            'c784a8b8ceceb3a453808a860a8dd9e0f8847f96cc82a7cc8410bc682aaadb06')

package() {
    install -Dm755 "$srcdir/acpid.initd" "$pkgdir/etc/init.d/acpid"
    install -Dm644 "$srcdir/acpid.confd" "$pkgdir/etc/conf.d/acpid"
}
