# Maintainer: artoo <artoo@artixlinux.org>
# Contributor: williamh <williamh@gentoo.org>

pkgname=openrc-settingsd
pkgver=1.1.0
pkgrel=2
pkgdesc="System settings D-Bus service for OpenRC"
arch=('i686' 'x86_64')
url="https://gitlab.com/postmarketOS/openrc-settingsd"
license=('GPL')
groups=('openrc-world')
depends=('libdaemon' 'openrc' 'polkit')
optdepends=('nss-myhostname: nss-myhostname module')
makedepends=('python' 'automake')
backup=('etc/conf.d/openrc-settingsd')
source=("https://gitlab.com/postmarketOS/openrc-settingsd/-/archive/v${pkgver}/${pkgname}-v${pkgver}.tar.gz")
sha256sums=('8be909a8a29e3661401d322ab1c390c03dc303888d44b9149dd07e4909a1a663')

prepare() {
    cd "${pkgname}-v${pkgver}"

    sed -i -e 's|/sbin/runscript|/usr/bin/openrc-run|g' data/init.d/openrc-settingsd.in
    sed -e 's|^dbusbusconfigdir = $(sysconfdir)|dbusbusconfigdir = $(datadir)|' \
        -i Makefile.am

    autoreconf -if
}

build(){
    cd "${pkgname}-v${pkgver}"
    ./configure \
        --sysconfdir=/etc \
        --prefix=/usr \
        --libdir=/usr/lib \
        --libexecdir=/usr/lib \
        --datarootdir=/usr/share \
        --localstatedir=/var \
        --sbindir=/usr/bin \
        --with-pidfile=/run/openrc-settingsd.pid
    make
}

check() {
    cd "${pkgname}-v${pkgver}"
    make check -k
}

package() {
    cd "${pkgname}-v${pkgver}"

    make DESTDIR="${pkgdir}" install

    install -Dm644 ${srcdir}/${pkgname}-v${pkgver}/COPYING "$pkgdir/usr/share/licenses/${pkgname}/COPYING"
}
