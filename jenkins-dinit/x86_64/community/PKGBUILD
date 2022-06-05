# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=jenkins-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for jenkins"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('jenkins' 'dinit')
conflicts=('init-jenkins')
provides=('init-jenkins')
source=("jenkins" "jenkins.script" "jenkins-pre")
sha256sums=('eed95f7d9f81b30d40051395dc28dae8e6d26cae24b204b19462ba2a9b9d8b48'
            '2af7e6e3f78e73c918600ce204e9428af64d3ec3497be70859f1680c77e2af32'
            'ff18ced7a72d6bcf452cfff1015d8af72313b48b1b3e9c838969ddbe2a715d14')

package() {
    install -Dm644 jenkins        "$pkgdir/etc/dinit.d/jenkins"
    install -Dm644 jenkins-pre    "$pkgdir/etc/dinit.d/jenkins-pre"
    install -Dm755 jenkins.script "$pkgdir/etc/dinit.d/scripts/jenkins"
}
