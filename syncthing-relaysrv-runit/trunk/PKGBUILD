# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/var/service|/run/runit/service|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=syncthing-relaysrv-runit
pkgver=20190202
pkgrel=3
pkgdesc="Runit service script for syncthing-relaysrv"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('syncthing-relaysrv' 'runit')
conflicts=('init-syncthing-relaysrv')
provides=('init-syncthing-relaysrv')
groups=('runit-galaxy')
source=("relaysrv.run::${_url}/syncthing/files/relaysrv/run"
        "logrelaysrv.run::${_url}/syncthing/files/relaysrv/log/run")
sha256sums=('79b76c3010b182aa9f7d17062b7b5e705157b19386e252967bf795c0113ec17c'
            '1ead1dd0b2e1a77d7dce1e48eef319548454db47c7e5a8a255e0cedf7a6164a6')

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
    sed -e 's|-u relaysrv|-u syncthing-relaysrv|g' -i "$srcdir/relaysrv.run"
    _inst_sv 'relaysrv'
    _inst_logsv 'relaysrv'
}
