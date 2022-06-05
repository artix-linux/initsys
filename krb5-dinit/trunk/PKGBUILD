# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=krb5-dinit
pkgver=20211029
pkgrel=2
pkgdesc="dinit service scripts for krb5"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-system')
depends=('krb5' 'dinit')
provides=('init-krb5')
conflicts=('init-krb5')
source=("kadmind"
        "krb5kdc")
sha256sums=('9f15e47c78cca36e2846572e2f32fb529a6c3973d06e8b367ae326dba20eb625'
            '9ebe10ac919dac8bfee50df5cdc8a60f238e34b57ec2591f057e5b20f7c9e62e')

package() {
    install -Dm644 kadmind "$pkgdir/etc/dinit.d/kadmind"
    install -Dm644 krb5kdc "$pkgdir/etc/dinit.d/krb5kdc"
}
