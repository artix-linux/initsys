# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/var/service|/run/runit/service|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=syncthing-runit
pkgver=20190202
pkgrel=4
pkgdesc="Runit service script for syncthing"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
# Note: While this PKGBUILD is licensed under BSD-3 terms, all of the
#       included runscript should follow it's main package's licenses.
depends=('syncthing' 'runit')
groups=('runit-galaxy')
install=syncthing-runit.install
provides=('init-syncthing')
conflicts=('init-syncthing')
source=("syncthing.run"
        "logsyncthing.run"
        "syncthing.conf")
sha256sums=('937c1c910f583e38bedf911d0ef522b6fc16998302d6d9cd4e313bdec65cad83'
            'cc524d6e190a19a70ca34b66520abec2060e08041589b34a3a1048b63e6bf4a4'
            '9af1ce2cf531c758a0a84f7e683172cac24081fbb2001d6e3125e512a214f03e')

_inst_logsv() {
    for file in run finish check; do
        if test -f "$srcdir/log$1.$file"; then
            install -Dm755 "$srcdir/log$1.$file" "$pkgdir/etc/runit/sv/$1/log/$file"
            sed "${_sed_args[@]}" -i "$pkgdir/etc/runit/sv/$1/log/$file"
        fi
    done
}

_inst_sv() {
    if test -f "$srcdir/$1.conf"; then
        install -Dm644 "$srcdir/$1.conf" "$pkgdir/etc/runit/sv/$1/conf"
    fi

    for file in run finish check; do
        if test -f "$srcdir/$1.$file"; then
            install -Dm755 "$srcdir/$1.$file" "$pkgdir/etc/runit/sv/$1/$file"
            sed "${_sed_args[@]}" -i "$pkgdir/etc/runit/sv/$1/$file"
        fi
    done
}

package() {
    _inst_sv 'syncthing'
    _inst_logsv 'syncthing'
}
