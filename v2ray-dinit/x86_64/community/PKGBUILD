# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=v2ray-dinit
pkgver=20211103
pkgrel=2
pkgdesc="dinit service scripts for v2ray"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('v2ray' 'dinit')
conflicts=('init-v2ray')
provides=('init-v2ray')
source=("v2ray")
sha256sums=('f6aa2ceb821206cc739b3fd7826184b6aaf48f31293339f7136ce2de5ac40ca4')

package() {
    install -Dm644 v2ray "$pkgdir/etc/dinit.d/v2ray"
}
