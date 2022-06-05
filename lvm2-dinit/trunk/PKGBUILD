# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=lvm2-dinit
pkgver=20211029
pkgrel=1
pkgdesc="dinit stage1 scripts for lvm2"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-system')
depends=('lvm2')
provides=('init-lvm2')
conflicts=('init-lvm2')
source=("lvm2-monitor"
        "lvm2"
        "lvmpolld"
        "lvmpolld.script")
sha256sums=('af2ba17663d24e0117536493a446a2c9d5700c65d0407f4e23bbb3f09fb74d0f'
            '27d6cb7b931eb22308032cdae72fab7ef1c8b161ceaa5683e5aeed2fad62955a'
            '04d91983c5a215a4a54c3a25a12efb77b91d5698c7bad004b6fb6ee35f9c9174'
            '80d54d6af7523962c9faad464752d39899bb72b7779ef65328c3cfb5acb528a9')

package() {
    install -Dm644 lvm2 "$pkgdir/etc/dinit.d/lvm2"
    mkdir -p "$pkgdir/etc/dinit.d/mount.d/"
    ln -s ../lvm2 "$pkgdir/etc/dinit.d/mount.d/lvm2"
    install -Dm644 lvm2-monitor "$pkgdir/etc/dinit.d/lvm-monitor"
    install -Dm644 lvmpolld "$pkgdir/etc/dinit.d/lvmpolld"
    install -Dm755 lvmpolld.script "$pkgdir/etc/dinit.d/scripts/lvmpolld"
}
