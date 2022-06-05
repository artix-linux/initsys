# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=rspamd-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for rspamd"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('rspamd' 'dinit')
conflicts=('init-rspamd')
provides=('init-rspamd')
source=("rspamd")
sha256sums=('3e1a4d99052bb52ad590554e82601b971cd67f6bcddafd2414f034505462d63f')

package() {
    install -Dm644 rspamd "$pkgdir/etc/dinit.d/rspamd"
}
