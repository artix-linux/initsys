# Maintainer: nous@artixlinux.org

pkgname=distcc-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC distcc init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'distcc')
provides=('init-distcc')
conflicts=('init-distcc')
backup=('etc/conf.d/distcc')
source=("distcc."{initd,confd})
sha256sums=('33a46db9bc3fa1ef084f24fd7778bdbfc0d5bff060e8b86f27642491b45b2c46'
            '4ce65bb986c4d97c22f03246488a1f1104b4cba5ea2f5eca649109b7af2ee0c1')

package() {
	install -Dm755 "$srcdir/distcc.initd" "$pkgdir/etc/init.d/distcc"
	install -Dm644 "$srcdir/distcc.confd" "$pkgdir/etc/conf.d/distcc"
}
