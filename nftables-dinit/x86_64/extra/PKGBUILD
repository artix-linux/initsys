# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=nftables-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service script for nftables"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('nftables' 'dinit')
groups=('dinit-world')
conflicts=('init-nftables')
provides=('init-nftables')
source=("nftables")
sha256sums=('5b7660f01f58588852ceabb728f70070c60768b546a319958f5787f434c59a33')

package() {
    install -Dm644 nftables "$pkgdir/etc/dinit.d/nftables"
}
