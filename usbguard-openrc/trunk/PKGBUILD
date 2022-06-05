# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=usbguard-openrc
pkgver=20210505
pkgrel=2
pkgdesc="openrc script for usbguard"
arch=('x86_64')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-usbguard')
depends=('openrc' 'usbguard')
conflicts=('init-usbguard')
source=('usbguard.initd')
sha256sums=('e1e889a3e785ed2f1213c25c2d400ececf8dd156ab9af79f229c081908294afe')
b2sums=('d468ac7d76ab3051c9edcee39b4ab02f8fb26f123470b620d235d65ebeb3517e3f3e53ee2eb692117efa7dfd4c0e16e01470327e6ff9a990a6540c4b093f4526')

package() {
    install -Dm755 "$srcdir"/usbguard.initd "$pkgdir"/etc/init.d/usbguard
}

# vim:set ts=2 sw=2 et:

