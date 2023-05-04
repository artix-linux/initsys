# Maintainer: Carlo den Otter <artist@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/var/service|/run/runit/service|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=v2ray-runit
pkgver=20230501
pkgrel=1
pkgdesc="Runit service script for v2ray"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
# Note: While this PKGBUILD is licensed under BSD-3 terms, all of the
#       included runscript should follow it's main package's licenses.
depends=('v2ray' 'runit')
groups=('runit-galaxy')
provides=('init-v2ray')
conflicts=('init-v2ray')
source=("v2ray.run")
sha256sums=('c3d87d35564aaa7fc84c2a957ca0af35955c06fbbe68673c9a9da9b6ef9e237c')

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
    _inst_sv 'v2ray'
}
