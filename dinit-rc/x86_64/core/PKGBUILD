# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>
pkgname=dinit-rc
pkgver=0.0.32
pkgrel=1
pkgdesc="rc files for dinit"
arch=('x86_64')
url="https://gitea.artixlinux.org/artix/dinit-rc"
license=('BSD')
depends=('udev')
provides=('init-udev' 'init-rc')
conflicts=('init-udev' 'init-rc')
backup=('etc/dinit.d/config/cgroups.conf'
        'etc/dinit.d/config/hwclock.conf'
        'etc/dinit.d/config/rc.local'
        'etc/dinit.d/config/rc.shutdown')
source=("$pkgname-$pkgver.tar.gz::${url}/archive/$pkgver.tar.gz")
sha256sums=('fbc6c5dd5b6c14d1a1fc15383e50120fc0e2f34e62a5ded60486ca571e24fcf1')

build() {
	cd "$pkgname"
	make
}

package() {
	cd "$pkgname"
	make DESTDIR="$pkgdir/" install

	# iputils
	mkdir -p "$pkgdir/usr/lib/sysctl.d"

	# copying
	install -Dm644 COPYING "$pkgdir/usr/share/licenses/dinit-rc/COPYING"
}
