# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=fwknop-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC fwknop init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'fwknop')
provides=('init-fwknop')
conflicts=('init-fwknop')
backup=('etc/conf.d/fwknop')
source=("fwknop."{confd,initd})
sha256sums=('818366d8012cf50771ab427bcf645de697e7d05e4bb80d5eb2f98291e071d510'
            '798e7100e8f7e78df46d33fa34c54ea6f81284cb7db46253592a8315ca452a6a')

package() {
    install -Dm755 "$srcdir/fwknop.initd" "$pkgdir/etc/init.d/fwknop"
    install -Dm644 "$srcdir/fwknop.confd" "$pkgdir/etc/conf.d/fwknop"
}
