# Maintainer: Chris Cromer <chris@cromer.cl>
# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

_commit=9f6718f5decadc794b2a9afcfff1a64e3afc166d

pkgname=runit-rc
pkgver=20210122
pkgrel=1
pkgdesc='Artix Linux system initialization and shutdown for runit'
arch=('x86_64')
url='https://gitea.artixlinux.org/artix/runit-rc'
license=('BSD')
makedepends=('git')
depends=('procps-ng' 'bash' 'bootlogd' 'eudev-runit')
provides=('init-rc')
conflicts=('init-rc')
source=("git+${url}.git#commit=$_commit")
sha256sums=('SKIP')
optdepends=('lvm2-runit: LVM support for runit'
            'cryptsetup-runit: Enable boot support for encrypted partitions')

build() {
	cd ${pkgname} #-${pkgver}
	make
}

package() {
	cd ${pkgname} #-${pkgver}
	make DESTDIR="${pkgdir}" install-rc

	# iputils-specific configuration
	mkdir -p "$pkgdir/usr/lib/sysctl.d"
	echo "net.ipv4.ping_group_range = 0 2147483647" > "$pkgdir/usr/lib/sysctl.d/55-iputils.conf"
}
