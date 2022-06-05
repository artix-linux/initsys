# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=lightdm-dinit
pkgver=20211030
pkgrel=3
pkgdesc="dinit service scripts for lightdm"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('lightdm' 'dbus-dinit')
provides=('init-lightdm' 'init-displaymanager')
conflicts=('init-lightdm' 'init-displaymanager')
source=("lightdm" "lightdm.script")
sha256sums=('669bf5c25c1fe156486bf28e7a41b9ce97206ae498545fa88bd505ecd1006e9a'
            'c6d87e5c593627b4b468ed1d92554407368e6584517ec8bb64c4c14344b480d7')

package() {
    install -Dm644 lightdm        "$pkgdir/etc/dinit.d/lightdm"
    install -Dm755 lightdm.script "$pkgdir/etc/dinit.d/scripts/lightdm"
}
