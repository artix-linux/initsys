# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=grafana-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for grafana"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('grafana' 'dinit')
conflicts=('init-grafana')
provides=('init-grafana')
source=("grafana")
sha256sums=('7f6a83b2584356722ddd49e15d7aaf26a6dd6b89556a39dde9483ef7324166c2')

package() {
    install -Dm644 grafana "$pkgdir/etc/dinit.d/grafana"
}
