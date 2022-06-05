# Maintainer: Carlo den Otter <artist@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/var/service|/run/runit/service|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=chrony-runit
pkgver=20200907
pkgrel=3
pkgdesc="Runit service script for chrony"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('chrony' 'runit')
groups=('runit-galaxy')
conflicts=('init-chrony' 'init-timed')
provides=('init-chrony' 'init-timed')
source=("chrony.run")
sha256sums=('c0a138f1b62a8b000cc8ec19deb4f8a0c45d6f87c869ececd2783c7501312fff')

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
    _inst_sv 'chrony'
}
