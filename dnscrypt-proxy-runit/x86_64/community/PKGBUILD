# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/var/service|/run/runit/service|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=dnscrypt-proxy-runit
pkgver=20210513
pkgrel=2
pkgdesc="runit service scripts for dnscrypt-proxy"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('dnscrypt-proxy' 'runit')
groups=('runit-galaxy')
conflicts=('init-dnscrypt-proxy')
provides=('init-dnscrypt-proxy')
source=("dnscrypt-proxy.run"
        "logdnscrypt-proxy.run")
sha256sums=('996bd42e23210cfadb1e9b5d8454ae52fc22ad0d86944afcc50790592a38fbfa'
            'bc789e33bd2571cf1d964764f6208136f525aa1eee3b406959df7f06b65089f6')

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
    _inst_sv 'dnscrypt-proxy'
    _inst_logsv 'dnscrypt-proxy'
}
