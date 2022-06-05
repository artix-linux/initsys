# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/var/service|/run/runit/service|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=salt-runit
pkgver=20180314
pkgrel=4
pkgdesc="Runit service script for salt"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('salt' 'runit')
groups=('runit-galaxy')
conflicts=('init-salt')
provides=('init-salt')
source=("salt-master.run"
        "salt-minion.run"
        "salt-api.run"
        "salt-syndic.run")
sha256sums=('677fecc601ce7ab64898b38d0f3e7d63beb9cf72f1380139b1316b9f600cee70'
            'fd8514f4741e4ca7a46c4bd0e4614c6906c5d84589515cf554977dcc27d5378e'
            '3cf87795872b701f5de7518f961b2253ce368df273283c3959c2b1ab4cb991df'
            'd98ae07db9ab328341e77ebd34f0a60f368d59c286193db034a06a8e1e977936')

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
    for f in master minion api syndic; do
        _inst_sv salt-$f
    done
}
