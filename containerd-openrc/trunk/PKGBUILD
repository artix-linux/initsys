# Maintainer: artoo <artoo@artixlinux.org>

pkgname=containerd-openrc
pkgver=20230512
pkgrel=1
pkgdesc="OpenRC containerd init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'containerd')
provides=('init-containerd')
conflicts=('init-containerd')
backup=('etc/conf.d/containerd')
source=("containerd.confd"
        "containerd.initd")
sha256sums=('f458b12e00a88af03dea82457b62d138f7e15d35f5014bc12f3a5b3e8848d225'
            'fa7745acb489b610e16e3c9890709493f8171a836fe9ff566c23385d5883d7b8')

package() {
     install -Dm755 "$srcdir/containerd.initd" "$pkgdir/etc/init.d/containerd"
     install -Dm644 "$srcdir/containerd.confd" "$pkgdir/etc/conf.d/containerd"
}
