# Maintainer: Carlo den Otter <artist@artixlinux.org>
# Contributor: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/var/service|/run/runit/service|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=spamassassin-runit
pkgver=20210417
pkgrel=2
pkgdesc="Runit service script for spamassassin"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('spamassassin' 'runit')
groups=('runit-world')
conflicts=('init-spamassassin')
provides=('init-spamassassin')
source=("spamd.run")
sha256sums=('cf29dec10d7a04307dc776785162091a00d41d6654513e2fe1361e35cee263fc')

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
    _inst_sv 'spamd'
}
