# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=firewalld-dinit
pkgver=20211101
pkgrel=1
pkgdesc="dinit service scripts for firewalld"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('firewalld' 'dinit' 'dbus-dinit')
conflicts=('init-firewalld')
provides=('init-firewalld')
source=("firewalld")
sha256sums=('4a0a093649985a9db5e4295a1555e35ca312d9c3fa088cb0140b841b7fadb41e')

package() {
    install -Dm644 firewalld "$pkgdir/etc/dinit.d/firewalld"
}
