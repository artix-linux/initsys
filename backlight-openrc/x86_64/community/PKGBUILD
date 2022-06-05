# Maintainer: Alois Nespor <alium@centrum.cz>

pkgname=backlight-openrc
pkgver=20210506
pkgrel=1
pkgdesc="Restore the screen brightness at system startup"
arch=('any')
license=('GPL3')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
groups=('openrc-galaxy')
provides=('init-backlight')
depends=('openrc')
conflicts=('init-backlight')
source=("backlight")
sha256sums=('07c97340e1a9ddc5b428ec4e256572df356fdcc1f28e1aa6beb114a2189774f4')

package() {
    install -Dm755 "$srcdir/backlight" "$pkgdir/etc/init.d/backlight"
}


