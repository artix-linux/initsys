# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=minio-dinit
pkgver=20211102
pkgrel=2
pkgdesc="dinit service scripts for minio"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-galaxy')
depends=('minio' 'dinit')
conflicts=('init-minio')
provides=('init-minio')
backup=('etc/dinit.d/config/minio.conf')
source=("minio" "minio-pre" "minio.script" "minio.conf" "minio-pre.script")
sha256sums=('63d433c26fbe95bb5c8048ad8041de7c08743ca17608e091dc7839f77d730db9'
            '073f3ae7140a5006ff71e22ce70db4794b96f40c897b8081954ad68bcc11acf9'
            'ea51e594c571bc4b3fd01dfa8b7a4d30064c5d39cdb1c7dfa08d7c939c1f4c97'
            'c2aae7c29901bfd7ab4819228e5793ca12ad519a02f05d4429e3c292ff8f1392'
            '0ab3faacce47b290fdd02637db53a69b05ae2603ab72b7e3a6063a3cca11ca9b')

package() {
    install -Dm644 minio            "$pkgdir/etc/dinit.d/minio"
    install -Dm644 minio-pre        "$pkgdir/etc/dinit.d/minio-pre"
    install -Dm644 minio.conf       "$pkgdir/etc/dinit.d/config/minio.conf"
    install -Dm755 minio.script     "$pkgdir/etc/dinit.d/scripts/minio"
    install -Dm755 minio-pre.script "$pkgdir/etc/dinit.d/scripts/minio-pre"
}
