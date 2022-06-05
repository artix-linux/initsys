# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=znc-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC ZNC init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'znc')
provides=('init-znc')
conflicts=('init-znc')
backup=('etc/conf.d/znc')
source=("znc.confd"
        "znc.initd")
sha256sums=('69238e187b86c4c15d0751a28d6710e3b21fdd19627b28d5ee09009dc1d95b01'
            'd9f8e0b4ddd7fc26b97816adf6ce8dade7b8c7065f3456b8bfb074dfaa6522c5')

package() {
    install -Dm755 "$srcdir/znc.initd" "$pkgdir/etc/init.d/znc"
    install -Dm644 "$srcdir/znc.confd" "$pkgdir/etc/conf.d/znc"
}
