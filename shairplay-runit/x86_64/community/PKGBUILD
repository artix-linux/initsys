# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/var/service|/run/runit/service|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=shairplay-runit
pkgver=20210407
pkgrel=5
pkgdesc="Runit service script for shairplay"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('shairplay' 'runit')
groups=('runit-galaxy')
provides=('init-shairplay')
conflicts=('init-shairplay')
backup=('etc/runit/sv/shairplay/conf')
source=("shairplay.run"
        "shairplay.conf")
sha256sums=('5bb884cc99f11f017c27d7168611812d0bcd7801eab83e7c815d0d5e3ff3c59d'
            '33490a6052a03ed26de277437f41aaaa3a168f9aa0c7e304e93b1969b0b2f39d')

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
    _inst_sv 'shairplay'
}
