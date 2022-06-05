# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=stunnel-openrc
pkgver=20210505
pkgrel=1
pkgdesc="openrc script for stunnel"
arch=('x86_64')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('stunnel' 'openrc')
provides=('init-stunnel')
conflicts=('init-stunnel')
source=('stunnel.initd'
        'stunnel.confd')
b2sums=('0b0e4c91afd4adff0612009e1d0e1070854eaa6dca2ce8d113153cbefec87155ed2ab2fc1909d70de4e5e875b7a664f05cda8df86d65bba9b32bfe1cf9ee5e12'
        'd57d0065b934a09bfc2a702f795a29aa2656135f3a1c87d2304421c272bf2185cc25a054c55100346b85b83b2e3b9b035a0375732e7cf6eeb01a03cc9695b4f1')

package() {
  cd "$srcdir"
  install -Dm755 stunnel.initd "$pkgdir"/etc/init.d/stunnel
  install -Dm644 stunnel.confd "$pkgdir"/etc/conf.d/stunnel
}

# vim:set ts=2 sw=2 et:
