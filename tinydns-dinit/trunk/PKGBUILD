# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=tinydns-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for tinydns"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('tinydns' 'dinit')
conflicts=('init-tinydns')
provides=('init-tinydns')
source=("tinydns")
sha256sums=('c53945aaed97cd57d197d43fd6f055e51483490190d05dd6e903be3d9e66fa92')

package() {
    install -Dm644 tinydns "$pkgdir/etc/dinit.d/tinydns"
}
