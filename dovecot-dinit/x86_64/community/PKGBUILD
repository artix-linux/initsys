# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=dovecot-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for dovecot"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('dovecot' 'dinit')
conflicts=('init-dovecot')
provides=('init-dovecot')
source=("dovecot" "dovecot.script")
sha256sums=('7ec6fb22b0dd9cc3001bc63e94f5f112b0c07d1dc14416b4f96417a297082443'
            'ebd698420378f87d51f418175bff87a07f2788b60acd34a86c98624e07b33239')

package() {
    install -Dm644 dovecot        "$pkgdir/etc/dinit.d/dovecot"
    install -Dm755 dovecot.script "$pkgdir/etc/dinit.d/scripts/dovecot"
}
