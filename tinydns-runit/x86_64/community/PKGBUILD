# Maintainer: Carlo den Otter <artist@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/var/service|/run/runit/service|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=tinydns-runit
pkgver=20201010
pkgrel=2
pkgdesc="Runit service script for tinydns"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
# Note: While this PKGBUILD is licensed under BSD-3 terms, all of the
#       included runscript should follow it's main package's licenses.
depends=('tinydns' 'runit')
groups=('runit-galaxy')
provides=('init-tinydns')
conflicts=('init-tinydns')
source=("tinydns.run")
sha256sums=('9d5bd9c38d0e032e4920b1e19a6c8c5f1d4f98e2e4f31e9354b77562c540f283')

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
    _inst_sv 'tinydns'
}
