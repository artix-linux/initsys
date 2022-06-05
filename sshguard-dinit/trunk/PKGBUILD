# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=sshguard-dinit
pkgver=20211102
pkgrel=1
pkgdesc="dinit service scripts for sshguard"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('sshguard' 'dinit')
conflicts=('init-sshguard')
provides=('init-sshguard')
source=("sshguard")
sha256sums=('f2b6b4cbcf640e7c38fccae7d777030a6aeeafacecef51b47f36672308d2dbbc')

package() {
    install -Dm644 sshguard "$pkgdir/etc/dinit.d/sshguard"
}
