# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=vsftpd-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for vsftpd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('vsftpd' 'dinit')
conflicts=('init-vsftpd')
provides=('init-vsftpd')
source=("vsftpd" "vsftpd-ipv6")
sha256sums=('9f76a2123fe9a7e87c2d1c3bbd56a0317ff35e97ba97f26b4d0ab61d1c13be05'
            '34c6922f22077724ebc33d8db623f79d2be66fea5f5b061ba03668d50c7f9575')

package() {
    install -Dm644 vsftpd      "$pkgdir/etc/dinit.d/vsftpd"
    install -Dm644 vsftpd-ipv6 "$pkgdir/etc/dinit.d/vsftpd-ipv6"
}
