# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=skalibs
pkgver=2.13.1.1
pkgrel=1
pkgdesc="A general-purpose utility library for secure, small C development"
url="http://www.skarnet.org/software/skalibs/"
license=('ISC')
arch=('x86_64')
depends=('glibc')
provides=('libskarnet.so')
source=(http://www.skarnet.org/software/$pkgname/$pkgname-$pkgver.tar.gz)
sha256sums=('b272a1ab799f7fac44b9b4fb5ace78a9616b2fe4882159754b8088c4d8199e33')

build() {
  cd ${pkgname}-${pkgver}
  ./configure --prefix=/usr \
      --datadir=/etc \
      --disable-static
  make
}

package() {
  cd ${pkgname}-${pkgver}
  make DESTDIR="$pkgdir" install
  install -D COPYING ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
}
