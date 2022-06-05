# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/service|/run/runit/service|g' -e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=cyrus-sasl-runit
pkgver=20180226
pkgrel=3
pkgdesc="runit service scripts for cyrus-sasl"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('runit-world')
depends=('cyrus-sasl' 'runit')
backup=('etc/runit/sv/saslauthd/conf')
conflicts=('init-cyrus-sasl')
provides=('init-cyrus-sasl')
source=("saslauthd.run"
        "saslauthd.conf")
sha256sums=('1d2682575f0134f6a0de20c9fbb606e4c8f72aa9ee357c31963bdc46abe5b774'
            'fa57b4f374ae633633091b1c8b44e1e0be814e4fddbfa75f16eb3dd1f16b8640')

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
    _inst_sv 'saslauthd'
}
