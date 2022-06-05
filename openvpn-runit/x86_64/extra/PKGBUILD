# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

_sed_args=(-e 's|/var/run|/run|g' -e 's|\(/usr\)\?/sbin|/usr/bin|g')

pkgname=openvpn-runit
pkgver=20180623
pkgrel=3
pkgdesc="runit service scripts for openvpn"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('openvpn')
backup=('etc/runit/sv/openvpn/conf')
install=openvpn-runit.install
source=("openvpn.run"
        "openvpn.conf")
sha256sums=('c1b7690a4da393c056b9b3de0a96553ca0b4895ef03924ab71245af49c3082b8'
            '6a91fe2d1895f92f0402b64c2ec0322b9591ffca21132b7f27bae7664c260f32')

_inst_sv(){
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
    _inst_sv 'openvpn'
}
