# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=lm_sensors-dinit
pkgver=20211030
pkgrel=3
pkgdesc="dinit service scripts for lm_sensors"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('lm_sensors' 'dinit')
conflicts=('init-lm_sensors')
provides=('init-lm_sensors')
source=("fancontrol"
        "lm_sensors"
        "lm_sensors.script")
sha256sums=('dfc2130e22a6fdf1c8f28d398d7e440240ca2a8c02dc4fbd02035c03f6f0ccb2'
            '1f916b5f71de00caf439aaf8996d9d3ed164a66e15940a5850c90382dfbb063e'
            'c5da0837a079f713fdde921031a168ab9c421d206b0c92a3f4af6e05fe79e437')

package() {
    install -Dm644 fancontrol        "$pkgdir/etc/dinit.d/fancontrol"
    install -Dm644 lm_sensors        "$pkgdir/etc/dinit.d/lm_sensors"
    install -Dm755 lm_sensors.script "$pkgdir/etc/dinit.d/scripts/lm_sensors"
}
