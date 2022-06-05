# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>

pkgname=dropbear-runit
pkgver=20191211
pkgrel=4
pkgdesc="Runit service script for dropbear"
arch=('any')
url="https://artixlinux.org"
groups=('runit-galaxy')
provides=('init-dropbear')
conflicts=('init-dropbear')
depends=('dropbear' 'runit')
source=("dropbear.run")
sha256sums=('74185d398ea3d99c7e44443d3c60f3dc2ec6ffa6a501f9e95db9e1ab58ea9d31')

_inst_sv() {
    for file in run finish check; do
        if test -f "$srcdir/$1.$file"; then
            install -Dm755 "$srcdir/$1.$file" "$pkgdir/etc/runit/sv/$1/$file"
        fi
    done
}

package() {
    _inst_sv 'dropbear'
}
