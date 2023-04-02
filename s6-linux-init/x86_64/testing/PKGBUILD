# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=s6-linux-init
pkgver=1.1.1.0
pkgrel=1
pkgdesc='A tool to automate the creation of suitable stage 1 init binaries for s6-based Linux systems.'
arch=('x86_64')
url='https://skarnet.org/software/s6-linux-init/'
license=('ISC')
depends=('s6' 'libs6.so')
provides=('libs6_linux_init.so')
backup=('etc/s6/current/scripts/rc.init'
        'etc/s6/current/scripts/rc.shutdown'
        'etc/s6/current/scripts/rc.shutdown.final'
        'etc/s6/current/scripts/runlevel')
source=("https://skarnet.org/software/${pkgname}/${pkgname}-${pkgver}.tar.gz"
        "rc.init"
        "rc.shutdown"
        "rc.shutdown.final"
        "runlevel")
sha256sums=('ad483f35326579007e5a7e3cb9f1fd1177eaf71ec5c11c47cd784a042956a8ee'
            '0e9cfda4e290314760b8d0915251e11d373e1a57851e9f68770d7d0f1f5bca44'
            'b8b5b7fc0de3c8870be83094071f3c82b98134a9223576e1c518bb8e7b6b5344'
            '524df97d15ea7cbcd885dd9a2e5af1f6411c41614e5c8125807412cc2e07c65a'
            '60b7dce044295b582da6eecf787c9633b84645e3714a6cc31d1d741c09986449')

build() {
  cd ${pkgname}-${pkgver}
  ./configure --prefix=/usr \
              --libexecdir=/usr/lib \
              --skeldir=/etc/s6/skel \
              --enable-shared \
              --disable-static
  make
}

package() {
  cd ${pkgname}-${pkgver}
  make DESTDIR="$pkgdir" install
  install -D -m644 COPYING "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"

  # default artix scripts
  install -Dm755 ${srcdir}/rc.init "${pkgdir}"/etc/s6/skel/rc.init
  install -Dm755 ${srcdir}/rc.shutdown "${pkgdir}"/etc/s6/skel/rc.shutdown
  install -Dm755 ${srcdir}/rc.shutdown.final "${pkgdir}"/etc/s6/skel/rc.shutdown.final
  install -Dm755 ${srcdir}/runlevel "${pkgdir}"/etc/s6/skel/runlevel

  # execute s6-linux-init-maker for PM tracking
  ./s6-linux-init-maker -1 -f "${pkgdir}"/etc/s6/skel -G "/usr/bin/agetty -L -8 tty7 115200" -c /etc/s6/current "${pkgdir}"/etc/s6/current
  mv "${pkgdir}"/etc/s6/current/bin/init "${pkgdir}"/etc/s6/current/bin/s6-init
  cp -a "${pkgdir}"/etc/s6/current/bin "${pkgdir}"/usr
  rm -r "${pkgdir}"/etc/s6/current/bin
}
