# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/var/service|/run/runit/service|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=wireguard-runit
pkgver=20201118
pkgrel=3
pkgdesc="Runit service script for wireguard"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('wireguard-tools' 'runit')
groups=('runit-world')
conflicts=('init-wireguard')
provides=('init-wireguard')
source=("wireguard.run"
        "wireguard.finish")
sha256sums=('db1067ffcf760ae705a5b38327afa5d95c8cffdef334c20c3e815496b1a8d33a'
            'f6ed0c12189f9297f53225bfaf1a44607ba36f54ed7f3503f5ac0c80dad53f1b')

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
    _inst_sv 'wireguard'
}
