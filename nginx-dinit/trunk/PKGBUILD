# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=nginx-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for nginx"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('nginx' 'dinit')
conflicts=('init-nginx')
provides=('init-nginx')
source=("nginx")
sha256sums=('7fe1ea8b5860f844d6bfc6359f8a58c1a874d3e724efd517deffac49b05ded71')

package() {
    install -Dm644 nginx "$pkgdir/etc/dinit.d/nginx"
}
