# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=boinc-openrc
pkgver=20210506
pkgrel=1
pkgdesc="OpenRC boinc init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('init-boinc')
depends=('openrc' 'boinc')
conflicts=('init-boinc')
backup=('etc/conf.d/boinc')
source=("boinc.confd"
        "boinc.initd")
sha256sums=('8919784d5212d187d50b4766bb75de9a5687f72bd42dab0dff86267313539c18'
            '87ab351a4215318d913518f68927847839d5fcf012724d7a81d12bc5b518128c')

package() {
    install -Dm755 "${srcdir}/boinc.initd" "${pkgdir}/etc/init.d/boinc"
    install -Dm644 "${srcdir}/boinc.confd" "${pkgdir}/etc/conf.d/boinc"
}
