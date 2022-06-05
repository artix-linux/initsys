# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=libvirt-dinit
pkgver=20211102
pkgrel=4
pkgdesc="dinit service scripts for libvirt"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('libvirt' 'dinit')
conflicts=('init-libvirt')
provides=('init-libvirt')
source=("libvirtd" "virtlockd" "virtlogd")
sha256sums=('a07c05b6d42f10a99b1400bc4f96ef65d008e97851ff7670de448e9407c60296'
            '7b0e09e0cd9bace2e39485e020523d321f4611d13d17bf35a33901f2ed91a52c'
            '8088ffec0d100ca8c30a5e12f46039cd138472132dcbe96bad7f5abebd010e6a')

package() {
    install -Dm644 libvirtd  "$pkgdir/etc/dinit.d/libvirtd"
    install -Dm644 virtlockd "$pkgdir/etc/dinit.d/virtlockd"
    install -Dm644 virtlogd  "$pkgdir/etc/dinit.d/virtlogd"
}
