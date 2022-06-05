# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=qemu-guest-agent-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service script for qemu-guest-agent"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('qemu-guest-agent' 'dinit')
groups=('dinit-world')
conflicts=('init-qemu-guest-agent')
provides=('init-qemu-guest-agent')
source=("qemu-ga")
sha256sums=('32f21654c0373e1c8d1edfb49ff7fbe2b908d5929445ab853fbec6d6445d0275')

package() {
    install -Dm644 qemu-ga "$pkgdir/etc/dinit.d/qemu-ga"
}
