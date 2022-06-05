# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/var/service|/run/runit/service|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=dns-over-https-runit
pkgver=20200425
pkgrel=3
pkgdesc="runit service scripts for dns-over-https"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('dns-over-https' 'runit')
provides=('init-dns-over-https')
conflicts=('init-dns-over-https')
groups=('runit-galaxy')
source=("doh-client.run"
        "doh-server.run")
sha256sums=('bb78ea4722819a7cc1397ed5c8d603e0eb9b0e4e85beb9e6662ab36b1382ead7'
            'a3d5caaab67c2533af7416b14619e7fc60f1d37e4604099e69961cd90d089d75')

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
    _inst_sv 'doh-client'
    _inst_sv 'doh-server'
}
