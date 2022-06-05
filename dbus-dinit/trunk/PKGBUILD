# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=dbus-dinit
pkgver=20211104
pkgrel=1
pkgdesc="dinit service scripts for dbus"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('dbus' 'dinit')
makedepends=('git')
provides=('init-dbus')
conflicts=('init-dbus')
groups=('dinit-system')
_commit=d2362e98e56dfe11308d1526c40f91f717e19a24
source=("dbus" "dbus-pre" "dbus-pre.script"
        "git+https://gitea.artixlinux.org/artix/alpm-hooks.git#commit=$_commit")
sha256sums=('06f33ca077cddae3fac9a86a4b77561e5fd4bb09df129a4b73b7578811c03d7e'
            'd146c81f268784e3e9f569dfea44bdc463a3eea997995e610c8d15947d7e027f'
            '81360807d31b2440f78631bb68ef0778576b8b0d297b5b16115ad8807f074bc5'
            'SKIP')

package() {
    install -Dm644 dbus "$pkgdir/etc/dinit.d/dbus"
    install -Dm644 dbus-pre "$pkgdir/etc/dinit.d/dbus-pre"
    install -Dm755 dbus-pre.script "$pkgdir/etc/dinit.d/scripts/dbus-pre"

    cd "$srcdir/alpm-hooks"
    make DESTDIR="$pkgdir" install_dinit_dbus
}
