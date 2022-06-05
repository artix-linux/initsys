# Maintainer: artoo <artoo@artixlinux.org>

pkgname=gdm-openrc
pkgver=20220104
pkgrel=1
pkgdesc="OpenRC gdm init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-displaymanager')
depends=('gdm' 'openrc')
conflicts=('init-displaymanager')
source=("gdm.initd")
sha256sums=('b46bb53bf9eb0c8d292133216af3c451060e8acc278e837d2bb5a58d548baec0')

package() {
    install -Dm755 "$srcdir/gdm.initd" "$pkgdir/etc/init.d/gdm"
}
