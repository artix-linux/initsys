# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=backuppc-dinit
pkgver=20211101
pkgrel=2
pkgdesc="dinit service scripts for backuppc"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('backuppc' 'dinit')
conflicts=('init-backuppc')
provides=('init-backuppc')
source=("backuppc")
sha256sums=('e4ec37c9b98c8233ab805fa70d784c83405b59cb92244a61d7d9193e86843347')

package() {
    install -Dm644 backuppc "$pkgdir/etc/dinit.d/backuppc"
}
