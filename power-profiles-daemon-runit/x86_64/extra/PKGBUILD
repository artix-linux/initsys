# Maintainer: Qontinuum <qontinuum@artixlinux.org>

pkgname=power-profiles-daemon-runit
_svc="${pkgname%-*}"
pkgver=20220503
pkgrel=1
pkgdesc="Runit service script for $_svc"
arch=(any)
url="https://gitea.artixlinux.org/packagesP/${pkgname}"
depends=("$_svc" dbus-runit)
groups=(runit-world)
provides=("init-$_svc")
conflicts=("init-$_svc")
source=("$_svc"{,.log}.run)
sha256sums=('18a6847646125a049689ae9d14e1d20fb5d5ade8bad180fd21ad27031e77d0c1'
            '86224b6df26a8b18d2c9e1b98892c59302b357e178a47411f919bf4f5ba00236')

package() {
    install -Dm755 "$srcdir/$_svc.run"     "$pkgdir/etc/runit/sv/$_svc/run"
    install -Dm755 "$srcdir/$_svc.log.run" "$pkgdir/etc/runit/sv/$_svc/log/run"
}
