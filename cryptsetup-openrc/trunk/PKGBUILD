# Maintainer: artoo <artoo@artixlinux.org>

pkgname=cryptsetup-openrc
pkgver=20211126
pkgrel=1
pkgdesc="OpenRC cryptsetup init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-system')
provides=('init-cryptsetup')
depends=('device-mapper-openrc' 'cryptsetup')
conflicts=('init-cryptsetup')
backup=('etc/conf.d/dmcrypt')
source=("dmcrypt.confd"
        "dmcrypt.initd")
sha256sums=('f2ca1396df6db52b4ba0a5138e77cae9219f8332c4803cdc7876741870bf3e01'
            '3c96ebf6735c1743733a6e648e2e92c693164bed5dec2d707f7233c4c2086ad7')

package() {
    install -Dm755 "${srcdir}"/dmcrypt.initd "${pkgdir}"/etc/init.d/dmcrypt
    install -Dm644 "${srcdir}"/dmcrypt.confd "${pkgdir}"/etc/conf.d/dmcrypt
}
