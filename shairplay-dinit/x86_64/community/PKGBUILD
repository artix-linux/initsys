# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=shairplay-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for shairplay"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('shairplay' 'dinit')
conflicts=('init-shairplay')
provides=('init-shairplay')
backup=('etc/dinit.d/config/shairplay.conf')
source=("shairplay" "shairplay.script" "shairplay.conf")
sha256sums=('a645dd4f46d83095cee4a93765dbb14a26c257c5e6f5343e6d83192bcc1acbf5'
            'c884c2d8e56274d6f3edaea9116f30e663dae86739dbd756ebc1125203857a98'
            '42edc9d3af3859a641e5050750229cf63ab932728633b775be11e1df6dc9cd33')

package() {
    # Due to shairplay config file containing password, it will be 600 instead of 644.
    install -Dm644 shairplay        "$pkgdir/etc/dinit.d/shairplay"
    install -Dm600 shairplay.conf   "$pkgdir/etc/dinit.d/config/shairplay.conf"
    install -Dm755 shairplay.script "$pkgdir/etc/dinit.d/scripts/shairplay"
}
