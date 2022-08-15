# Maintainer: Qontinuum <qontinuum@artixlinux.org>
# Contributor: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=gdm-runit
pkgver=20220815
pkgrel=1
pkgdesc="runit service scripts for gdm"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('runit-world')
depends=('gdm' 'init-logind')
provides=('init-gdm' 'init-displaymanager')
conflicts=('init-gdm' 'init-displaymanager')
source=("gdm.run")
sha256sums=('8db646a9f1e8573f77c147ae69f0188f663ae3b47d8c0bb7eb1dced9bafc055f')

package() {
    install -Dm755 gdm.run "$pkgdir/etc/runit/sv/gdm/run"
}
