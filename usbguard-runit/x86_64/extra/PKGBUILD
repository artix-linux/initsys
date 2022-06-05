# Maintainer: Carlo den Otter <artist@artixlinux.org>
# Contributor: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/var/service|/run/runit/service|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=usbguard-runit
pkgver=20210103
pkgrel=4
pkgdesc="Runit service script for usbguard"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('usbguard' 'runit')
groups=('runit-world')
conflicts=('init-usbguard')
provides=('init-usbguard')
source=("usbguard.run")
sha256sums=('affcad10f6ab033f540e198467b31aff462f7883a3abe1f6574e1eb7ca8a544c')

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
    _inst_sv 'usbguard'
}
