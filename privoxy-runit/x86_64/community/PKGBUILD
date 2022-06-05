# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/var/service|/run/runit/service|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=privoxy-runit
pkgver=20180314
pkgrel=5
pkgdesc="Runit service script for privoxy"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('privoxy' 'runit')
groups=('runit-galaxy')
conflicts=('init-privoxy')
provides=('init-privoxy')
source=("privoxy.run"
        "logprivoxy.run")
sha256sums=('5cb2368923b02c24d89a3a60ee5ebca41dfe60c975129d220f2f792529cc5731'
            'bc71f18b949e684213fd29096ba176accdca3213769d88e5daea638cabf5a316')

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
    _inst_sv 'privoxy'
    _inst_logsv 'privoxy'
}
