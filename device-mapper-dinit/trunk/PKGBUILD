# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=device-mapper-dinit
pkgver=20211029
pkgrel=1
pkgdesc="dinit service scripts for device-mapper"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-system')
depends=('device-mapper' 'dinit')
provides=('init-device-mapper')
conflicts=('init-device-mapper')
source=("dmeventd")
sha256sums=('e6b8c4b5a0573910a76ff8a82c1a60fe1e741ec62f6372794e0a93f112177a6e')

package() {
    install -Dm644 dmeventd "$pkgdir/etc/dinit.d/dmeventd"
}
