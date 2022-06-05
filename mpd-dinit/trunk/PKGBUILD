# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=mpd-dinit
pkgver=20211030
pkgrel=1
pkgdesc="dinit service scripts for mpd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('mpd' 'dinit')
conflicts=('init-mpd')
provides=('init-mpd')
source=("mpd" "mpd.script")
sha256sums=('d1e51922ffe7e3a395d8d4c10669b89232a76dc99b05ad6e3cadcc34072ea9cf'
            'c52bd3ca4641d50ad6222d3e4e88df59ddc8ca0807d1647b162fab2c3e1d1d08')

package() {
    install -Dm644 mpd        "$pkgdir/etc/dinit.d/mpd"
    install -Dm755 mpd.script "$pkgdir/etc/dinit.d/scripts/mpd"
}
