# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=darkhttpd-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for darkhttpd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('darkhttpd' 'dinit')
conflicts=('init-darkhttpd')
provides=('init-darkhttpd')
backup=('etc/dinit.d/config/darkhttpd.conf')
source=("darkhttpd" "darkhttpd.conf" "darkhttpd.script")
sha256sums=('68a7c15c822e7a34657d62cdd157b1a5c1379d349b0630367cced2b74a0a2c09'
            '47c77d6c4059ee1e9985205e82866b394dc48a307e9a94f5c14c051ef29f37ef'
            'b8bdf36e0002b0419697e1490e646e78c41113bba17f4eaf5726cb388e976919')

package() {
    install -Dm644 darkhttpd        "$pkgdir/etc/dinit.d/darkhttpd"
    install -Dm644 darkhttpd.conf   "$pkgdir/etc/dinit.d/config/darkhttpd.conf"
    install -Dm755 darkhttpd.script "$pkgdir/etc/dinit.d/scripts/darkhttpd"
}
