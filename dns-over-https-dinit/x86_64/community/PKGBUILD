# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=dns-over-https-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for dns-over-https"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('dns-over-https' 'dinit')
conflicts=('init-dns-over-https')
provides=('init-dns-over-https')
source=("doh-client" "doh-server")
sha256sums=('4424de9eaf614f08d4b8b4a2acb34af27c415686272b727b93bf5c641f423dc2'
            'dede407ade68c74cd2ac218a985b7d98d3b4fedafd1c3726aeb82df41a0b65ea')

package() {
    install -Dm644 doh-client "$pkgdir/etc/dinit.d/doh-client"
    install -Dm644 doh-server "$pkgdir/etc/dinit.d/doh-server"
}
