# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=fuse-dinit
pkgver=20211030
pkgrel=1
pkgdesc="dinit service scripts for fuse"
arch=('any')
url="https://artixlinux.org"
groups=('dinit-world')
provides=('init-fuse')
conflicts=('init-fuse')
depends=('fuse' 'dinit')
source=("fuse" "fuse.script")
sha256sums=('0d7010f7f6a5f946d1daa6bc4562d378c8c78c2e52d8b4d52308e55343e4d85e'
            '8501b8ebac992a3fc0abba63c73b1d7f003d451cc1190fea10a9eb0b4a8a4da6')

package() {
    install -Dm644 fuse        "$pkgdir/etc/dinit.d/fuse"
    install -Dm755 fuse.script "$pkgdir/etc/dinit.d/scripts/fuse"
}
