# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=webhook-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for webhook"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('webhook' 'dinit')
conflicts=('init-webhook')
provides=('init-webhook')
source=("webhook")
sha256sums=('0980f216485ef55d0a7279f1af3c52efa7e13eeb2d3b72bd3227fb41a66d9406')

package() {
    install -Dm644 webhook "$pkgdir/etc/dinit.d/webhook"
}
