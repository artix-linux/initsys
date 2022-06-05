# Maintainer: artoo <artoo@artixlinux.org>
# Maintainer: nous <nous@artixlinux.org>

_pkgname=gitea
pkgname=gitea-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC Gitea init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'gitea')
provides=('init-gitea')
conflicts=('init-gitea')
backup=('etc/conf.d/gitea')
source=("gitea.confd"
        "gitea.initd")
sha256sums=('1006c19591b1c2a674d83d08517e484219cb4f1ac29b7301245a52454a156a4c'
            '6b2e0a99d6ddc9f8626766cba7bb1d77a3598099ec7311b6f57ef287232e4e80')

package() {
  install -Dm0644 "${srcdir}/${_pkgname}.confd" "${pkgdir}/etc/conf.d/${_pkgname}"
  install -Dm0755 "${srcdir}/${_pkgname}.initd" "${pkgdir}/etc/init.d/${_pkgname}"
}
