# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=atftp-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for atftp"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('atftp' 'dinit')
conflicts=('init-atftp')
provides=('init-atftp')
source=("atftpd")
sha256sums=('7706c22daab7b1f9c97bdc4c8ab4ca059b7b8feee6e5061b4694c54c65a2bfe3')

package() {
    install -Dm644 atftpd "$pkgdir/etc/dinit.d/atftpd"
}
