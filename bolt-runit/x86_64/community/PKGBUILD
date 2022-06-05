# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|\(/usr\)\?/sbin|/usr/bin|g')

pkgname=bolt-runit
pkgver=20210426
pkgrel=1
pkgdesc="runit service scripts for bolt"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('dbus-runit' 'bolt')
provides=('init-bolt')
conflicts=('init-bolt')
source=("boltd.run")
sha256sums=('326a5f2c5534794f4b8cdf99ba055749dc9f00605b2b525ce442285c792f23c1')

_inst_sv(){
    for file in run finish check; do
        if test -f "$srcdir/$1.$file"; then
            install -Dm755 "$srcdir/$1.$file" "$pkgdir/etc/runit/sv/$1/$file"
            sed "${_sed_args[@]}" -i "$pkgdir/etc/runit/sv/$1/$file"
        fi
    done
}

package() {
    _inst_sv 'boltd'

    install -d "${pkgdir}/etc/runit/runsvdir/default"
    ln -sf "/etc/runit/sv/bolt" "${pkgdir}/etc/runit/runsvdir/default/bolt"
}
