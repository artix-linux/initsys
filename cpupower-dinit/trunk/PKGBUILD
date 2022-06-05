# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=cpupower-dinit
pkgver=20211101
pkgrel=1
pkgdesc="dinit service scripts for cpupower"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('cpupower' 'dinit')
conflicts=('init-cpupower')
provides=('init-cpupower')
source=("cpupower" "cpupower.script")
sha256sums=('ddec63807ca14c18c9c7a11f495c13c2e203390a6c7517d5764b73f3b62b27b0'
            '9dc13d4b12eaa7605b80c28940489cce4a56e7b22e0c2d2ba3839361af4d8485')

package() {
    install -Dm644 cpupower        "$pkgdir/etc/dinit.d/cpupower"
    install -Dm755 cpupower.script "$pkgdir/etc/dinit.d/scripts/cpupower"
}
