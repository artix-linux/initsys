# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=ejabberd-dinit
pkgver=20220424
pkgrel=1
pkgdesc="dinit service scripts for ejabberd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('ejabberd' 'dinit')
provides=('init-ejabberd')
conflicts=('init-ejabberd')
source=("ejabberd" "ejabberd.script")
sha256sums=('2f49d718ec2b74eb91283a2042fc770162c275766fa5e28006357c62c42bdf6f'
            'ed9a8ad1b44726a3910e45ad889c269feb0ae721824a4edc487553d3e58cbadc')

package() {
    install -Dm644 ejabberd        "$pkgdir/etc/dinit.d/ejabberd"
    install -Dm755 ejabberd.script "$pkgdir/etc/dinit.d/scripts/ejabberd"
}
