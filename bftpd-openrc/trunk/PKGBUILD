# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=bftpd-openrc
pkgver=20210506
pkgrel=1
pkgdesc="OpenRC init script for bftpd"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-bftpd')
depends=('openrc' 'bftpd')
conflicts=('init-bftpd')
source=('bftpd')
b2sums=('4a9f23e16e889e2fc78c5ec59d2ffea55db1aa55a0367f5e55f32e06a384108bac3317c632fbba3a58bb0fb609bddb5f3cae4ed784f27d81582f589b3a16c8fb')

package() {
  install -Dm755 "${srcdir}"/bftpd -t "${pkgdir}"/etc/init.d
}

# vim:set ts=2 sw=2 et:
