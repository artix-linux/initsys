# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=acpid-dinit
pkgver=20211026
pkgrel=1
pkgdesc="dinit service script for acpid"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('acpid' 'dinit')
groups=('dinit-galaxy')
provides=('init-acpid')
conflicts=('init-acpid')
source=("acpid")
sha256sums=('aa18a2cdafb94a91820f48074e9065c4aa02ad596a0f51c345d7094d485995d4')

package() {
    install -Dm644 acpid "$pkgdir/etc/dinit.d/acpid"
}
