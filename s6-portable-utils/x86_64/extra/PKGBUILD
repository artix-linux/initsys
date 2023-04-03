# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=s6-portable-utils
pkgver=2.3.0.2
pkgrel=1
pkgdesc='Tiny portable generic utilities.'
arch=('x86_64')
url='https://skarnet.org/software/s6-portable-utils/'
license=('ISC')
depends=('skalibs')
source=("https://skarnet.org/software/${pkgname}/${pkgname}-${pkgver}.tar.gz")
sha256sums=('8714269134f012650daac040e5646372dea5658b9c0d89a7ca03bb2abec4d1e8')
build() {
  cd ${pkgname}-${pkgver}
  ./configure --prefix=/usr \
              --datadir=/etc \
              --libexecdir=/usr/lib \
              --enable-shared
  make
}

package() {
  cd ${pkgname}-${pkgver}
  make DESTDIR="$pkgdir" install
  install -Dm644 COPYING "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
} 
