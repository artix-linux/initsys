# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=openssh-dinit
pkgver=20211026
pkgrel=2
pkgdesc="dinit service scripts for openssh"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('openssh' 'dinit')
provides=('init-openssh')
conflicts=('init-openssh')
groups=('dinit-system')
source=("sshd" "sshd.script")
sha256sums=('2759fe5eaf648d8ad751cb43b7e7b2d013a6c6d75d1d84dab71224984194b698'
            'd0f51c16892230a68f7882897ea91b8e1a0dd9f1fe7a38e1bd006e6243806aa2')

package() {
    install -Dm644 sshd        "$pkgdir/etc/dinit.d/sshd"
    install -Dm755 sshd.script "$pkgdir/etc/dinit.d/scripts/sshd"
}
