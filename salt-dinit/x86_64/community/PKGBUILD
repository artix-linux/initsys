# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=salt-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for salt"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('salt' 'dinit')
conflicts=('init-salt')
provides=('init-salt')
source=("salt-master"
        "salt-api"
        "salt-minion"
        "salt-syndic")
sha256sums=('4b55304278f29efccddd924a192f55f91ae0bd4264c5efb595f1fe214b50776b'
            '2ae2b1f97efe54f4fec6d7539d7642ad4446e51f170c79bbc013caa0f14bd9a7'
            '73cafbe9eb9d8ad0cb41b66981af95a6ca4142c83aa3296fc5bdc66c96b18e98'
            '0d2a74b299463172fb8edd77081b440b5cac9a0a483fe55d3354ab67f6177a0a')

package() {
    install -Dm644 salt-master "$pkgdir/etc/dinit.d/salt-master"
    install -Dm644 salt-api    "$pkgdir/etc/dinit.d/salt-api"
    install -Dm644 salt-minion "$pkgdir/etc/dinit.d/salt-minion"
    install -Dm644 salt-syndic "$pkgdir/etc/dinit.d/salt-syndic"
}
