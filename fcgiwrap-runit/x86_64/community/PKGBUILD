# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/service|/run/runit/service|g' -e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=fcgiwrap-runit
pkgver=20211208
pkgrel=1
pkgdesc="runit service scripts for fcgiwrap"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('runit-galaxy')
depends=('fcgiwrap' 'runit')
conflicts=('init-fcgiwrap')
provides=('init-fcgiwrap')
source=("fcgiwrap.run" "fcgiwrap.finish")
sha256sums=('d2e7a07902d826d257817ffc673f2ae607aa8ba3a51c0d384e95fb14e55fb82d'
            'd33604ec38f125fc86b948d1332756994e674ae833f49f7315b954f7cb9cf131')

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
    _inst_sv 'fcgiwrap'
}
