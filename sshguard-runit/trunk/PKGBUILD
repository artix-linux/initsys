# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|/usr/sbin|/usr/bin|g' -e 's|/opt/bin|/usr/bin|g' -e 's|/var/service|/run/runit/service|g' -e 's|/usr/libexec|/usr/lib|g')

pkgname=sshguard-runit
pkgver=20210504
pkgrel=1
pkgdesc="Runit service script for sshguard (using socklog)"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('sshguard' 'socklog' 'iptables-runit')
groups=('runit-galaxy')
conflicts=('init-sshguard')
provides=('init-sshguard')
source=("sshguard-socklog.run")
sha256sums=('e32bb88d9f54323b355d96ec451f0462c2a5475e46e66dde6bb6b0669f0e34c6')

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
    sed -e 's|socklog-unix|socklog|g' \
        -i "$srcdir/sshguard-socklog.run"

    _inst_sv 'sshguard-socklog'
}
