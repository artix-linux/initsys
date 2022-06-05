# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=audit-dinit
pkgver=20211031
pkgrel=2
pkgdesc="dinit service script for audit"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
depends=('audit' 'dinit')
groups=('dinit-system')
conflicts=('init-audit')
provides=('init-audit')
backup=('etc/dinit.d/config/auditctl.conf')
source=("auditd"
        "auditctl"
        "auditctl.script"
        "auditctl.conf")
sha256sums=('01894c6e947b13f92f103f01efb79c5b5d8ee27df1f2424e2fe294b3b9b0391e'
            'a64e63b8829f3d153e4ef86cb6cb16027ab7576a13200e3a65d8862af82b10f1'
            '321281306004be041a9adc6255b7112e22351352675072db0cc96e499fd4be5c'
            '67adef67c32704dcaf62d8ab827467647253de7b38e0254ec5120b8b87357015')

package() {
    install -Dm644 auditd          "$pkgdir/etc/dinit.d/auditd"
    install -Dm644 auditctl        "$pkgdir/etc/dinit.d/auditctl"
    install -Dm644 auditctl.conf   "$pkgdir/etc/dinit.d/config/auditctl.conf"
    install -Dm755 auditctl.script "$pkgdir/etc/dinit.d/scripts/auditctl"
}
