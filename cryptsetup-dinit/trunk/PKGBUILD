# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=cryptsetup-dinit
pkgver=20211025
pkgrel=1
pkgdesc="dinit stage1 script for cryptsetup"
arch=('any')
url="https://artixlinux.org"
license=('MIT')
groups=('dinit-system')
provides=('init-cryptsetup')
depends=('cryptsetup' 'dinit-rc')
conflicts=('init-cryptsetup')
source=('cryptsetup' 'cryptsetup-script')
optdepends=('lvm2-dinit: LVM support for encrypted filesystems')
sha256sums=('0593ce387724adaab6d69b87f695c7802ab3069bfe69bf45f5314b358ca2f494'
            'd45e31ff41d0398de50a169cf995f32bfde4ab69dbb2d3c820d24b2d6fb09cd3')

package() {
    install -Dm644 "${srcdir}/cryptsetup" "${pkgdir}/etc/dinit.d/cryptsetup"
    install -Dm755 "${srcdir}/cryptsetup-script" "${pkgdir}/etc/dinit.d/scripts/cryptsetup"

    mkdir -p "$pkgdir/etc/dinit.d/mount.d"
    ln -sf ../cryptsetup "$pkgdir/etc/dinit.d/mount.d"
}
