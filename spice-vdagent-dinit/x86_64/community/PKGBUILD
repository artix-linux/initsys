# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=spice-vdagent-dinit
pkgver=20211102
pkgrel=3
pkgdesc="dinit service scripts for spice-vdagent"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('spice-vdagent' 'dinit')
conflicts=('init-spice-vdagent')
provides=('init-spice-vdagent')
source=("spice-vdagentd" "spice-vdagentd.script")
sha256sums=('0871cfb4259b5d21c90497220c97c0206d4c3cda01aa84fdfdd80dc7a1a3dbf6'
            '10485875b39529ef61bb31323d73d1093ff545552e726637938b3cc31791f343')

package() {
    install -Dm644 spice-vdagentd        "$pkgdir/etc/dinit.d/spice-vdagentd"
    install -Dm755 spice-vdagentd.script "$pkgdir/etc/dinit.d/scripts/spice-vdagentd"
}
