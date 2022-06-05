# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=lxdm-s6
pkgver=20220410
pkgrel=1
pkgdesc="s6-rc service scripts for lxdm"
arch=('any')
url="https://gitea.artixlinux.org/artix/s6-services"
groups=('s6-galaxy')
provides=('init-lxdm')
conflicts=('init-lxdm')
depends=('lxdm-gtk3' 's6-base')
makedepends=('git')
install=lxdm.install
_commit=ae8411503d26202deef5e47f1ea7bc5ca30d23ff
source=("git+https://gitea.artixlinux.org/artix/s6-services.git#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd "${srcdir}"/s6-services
    sh install.sh "lxdm" "${pkgdir}"

    # hack for upgrading from a really old version
    rm "${pkgdir}"/etc/s6/sv/lxdm-log/pipeline-name
    mkdir -p "${pkgdir}"/etc/s6/sv/lxdm/contents.d
    touch "${pkgdir}"/etc/s6/sv/lxdm/contents.d/{lxdm-log,lxdm-srv}
    echo "bundle" > "${pkgdir}"/etc/s6/sv/lxdm/type
}
