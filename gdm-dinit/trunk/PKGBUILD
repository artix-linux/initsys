# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=gdm-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for gdm"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('gdm' 'dbus-dinit')
provides=('init-gdm' 'init-displaymanager')
conflicts=('init-gdm' 'init-displaymanager')
source=("gdm" "gdm.script")
sha256sums=('8e946260163ea86d6fa80c709f44c959f52c4cbc1f4f58d9fec7428da200d6ec'
            'e51bcec3f62565ca173025014ed6d20537aeeda827cc6e987f6623ba0e0489e4')

package() {
    install -Dm644 gdm        "$pkgdir/etc/dinit.d/gdm"
    install -Dm755 gdm.script "$pkgdir/etc/dinit.d/scripts/gdm"
}
