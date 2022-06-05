# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=hdparm-dinit
pkgver=20211029
pkgrel=1
pkgdesc="dinit stage1 script for hdparm"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-system')
provides=('init-hdparm')
depends=('hdparm' 'dinit-rc')
conflicts=('init-hdparm')
backup=('etc/dinit.d/config/hdparm.conf')
source=('hdparm' 'hdparm.script' 'hdparm.conf')
sha256sums=('4eca166b41c932ee401a1e31a0af4ef40b1dd7b4d3227e286c8a25e03493ec2f'
            '79d09b7e3e39de1cb0b075328d99592dfa71ac2e730f96f87f0dd9267644892f'
            'd205154cd4378428ee9977d1d525ee7774797924ba9ff0f88bec27af8aa08ecf')

package() {
    install -Dm644 hdparm        "$pkgdir/etc/dinit.d/hdparm"
    install -Dm644 hdparm.conf   "$pkgdir/etc/dinit.d/config/hdparm.conf"
    install -Dm755 hdparm.script "$pkgdir/etc/dinit.d/scripts/hdparm"
}
