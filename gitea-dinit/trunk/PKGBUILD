# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=gitea-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for gitea"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('gitea' 'dinit')
conflicts=('init-gitea')
provides=('init-gitea')
source=("gitea")
sha256sums=('e6dd1b55162a1472b69e2b61f6d8b2e9a7f40a2c56bb78a78e8335b4e1d9972c')

package() {
    install -Dm644 gitea "$pkgdir/etc/dinit.d/gitea"
}
