# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=backlight-runit
pkgver=20200420
pkgrel=4
pkgdesc="runit service scripts for backlight"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('runit-galaxy')
depends=('runit')
provides=('init-backlight')
conflicts=('init-backlight')
source=("backlight.run"
        "backlight.finish")
sha256sums=('d60221218641d2be6bc589c5b5c37e76ae8ad7b3f380b3d883197164cea5cff8'
            'ba0b1b086b7275f536258be1e01fc2f4ac8e1331365bff77ac27444f4f24785e')

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
    _inst_sv 'backlight'
}
