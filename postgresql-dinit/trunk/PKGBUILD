# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=postgresql-dinit
pkgver=20211030
pkgrel=3
pkgdesc="dinit service scripts for postgresql"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('postgresql' 'dinit')
conflicts=('init-postgresql')
provides=('init-postgresql')
backup=('etc/dinit.d/config/postgres.conf')
source=("postgres"
        "postgres.script"
        "postgres.conf"
        "postgres-pre"
        "postgres-pre.script")
sha256sums=('89f1be65d4cda6a0c9c399793230beea9840fd7a91d58b2f32e50a0e1c9f238f'
            'f00f63404f610e6d730b8b461a940e5583017e596a457221a43bbef4e5ddf6fc'
            '79e887e893965bf8c3a6e4cf6d7d1a8825f24160b45f948d1d882f4b049f075d'
            '5146e74f5ecbbf8531c922a9170559025fa0b3c68f1951aacc21f80a5362d07c'
            '44777ddbdeda2dfec690d49983f8a15835e0058e06b9a0d95830b9f8d5ced672')

package() {
    install -Dm644 postgres            "$pkgdir/etc/dinit.d/postgres"
    install -Dm644 postgres.conf       "$pkgdir/etc/dinit.d/config/postgres.conf"
    install -Dm755 postgres.script     "$pkgdir/etc/dinit.d/scripts/postgres"
    install -Dm644 postgres-pre        "$pkgdir/etc/dinit.d/postgres-pre"
    install -Dm755 postgres-pre.script "$pkgdir/etc/dinit.d/scripts/postgres-pre"
}
