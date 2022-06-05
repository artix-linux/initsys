# Maintainer: Qontinuum <qontinuum@artixlinux.org>
# Contributor: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=acpid-runit
pkgver=20220314
pkgrel=1
pkgdesc='Runit service script for acpid'
arch=('any')
url='https://artixlinux.org'
license=('BSD')
depends=('acpid' 'runit')
groups=('runit-galaxy')
provides=('init-acpid')
conflicts=('init-acpid')
install='acpid-runit.install'
source=('acpid.run' 'acpid.log.run')
b2sums=('9fcd9e23cc720710d36159d6ce7c77aeaadb67368a231a69c0b9217f9c39d887ae7dbf3fa2d75eb3f4c30dc82b49469699e7b791cd5801eaa7a11c95f627c05e'
        '83d4fae048494ebf8ef6ef27ae99d12416b6aa8ecfe3bf197fb7e6d9f8f62dc3d71d255cf920d99e114ea95cf1234fa2956879feb80fc2a4f3d53604ff4d01e2')

package() {
    cd "$srcdir"

    install -Dm755 acpid.run "$pkgdir/etc/runit/sv/acpid/run"
    install -Dm755 acpid.log.run "$pkgdir/etc/runit/sv/acpid/log/run"
}
