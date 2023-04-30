# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=redis-dinit
pkgver=20230429
pkgrel=1
pkgdesc="dinit service scripts for redis"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('redis' 'dinit')
conflicts=('init-redis')
provides=('init-redis')
source=("redis" "redis.script")
sha256sums=('58f814f0851b3a8c7c598eb976aafa6f33e19142b035338f7dc738877f9053af'
            '869c1617e15274b6cfa0f1a1aa6cb8e51e5ee63144f7b6f213eeb5910eeb5360')

package() {
    install -Dm644 redis        "$pkgdir/etc/dinit.d/redis"
    install -Dm755 redis.script "$pkgdir/etc/dinit.d/scripts/redis"
}
