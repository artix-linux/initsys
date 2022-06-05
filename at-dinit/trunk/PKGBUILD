# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=at-dinit
pkgver=20211101
pkgrel=1
pkgdesc="dinit service scripts for at"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('at' 'dinit')
makedepends=('git')
conflicts=('init-at')
provides=('init-at')
_commit=185c4b2e51cf46d99b474af9018c25039d7092a8
source=("atd"
        "git+https://gitea.artixlinux.org/artix/alpm-hooks.git#commit=$_commit")
sha256sums=('dab58c5b40f306854ede59a813d8517bf951da215f655323b92ba478128bea3d'
            'SKIP')

package() {
    install -Dm644 atd "$pkgdir/etc/dinit.d/atd"

    cd "$srcdir/alpm-hooks"
    make DESTDIR="$pkgdir" install_dinit_at
}
