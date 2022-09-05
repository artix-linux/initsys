# Maintainer: Dudemanguy <dudemanguy@artixlinux.org>
pkgname=s6-scripts
pkgver=20220905
pkgrel=1
pkgdesc='A collection of essential s6-rc oneshots and longruns for startup/shutdown.'
arch=('any')
url='https://gitea.artixlinux.org/artix/s6-scripts'
provides=('init-udev' 'eudev-s6')
depends=('execline' 'pam' 's6-rc' 'udev')
makedepends=('git')
optdepends=('cryptsetup-s6: cryptsetup boot script support'
            'lvm2-s6: lvm2 boot script support')
replaces=('eudev-s6')
backup=('etc/s6/rc.local'
        'etc/s6/config/tty1.conf'
        'etc/s6/config/tty2.conf'
        'etc/s6/config/tty3.conf'
        'etc/s6/config/tty4.conf'
        'etc/s6/config/tty5.conf'
        'etc/s6/config/tty6.conf'
        'etc/s6/config/ttyS.conf'
        'etc/s6/config/dmesg.conf'
        'etc/s6/config/hwclock.conf'
        'etc/s6/config/mount-cgroups.conf'
        'etc/s6/config/mount-tmpfs.conf'
        'etc/s6/config/udevd.conf'
        'usr/lib/sysctl.d/50-default.conf')
_commit=62175d9fdfe156bfc04c666963cdcaca6b790f03
source=("git+https://gitea.artixlinux.org/artix/s6-scripts.git#commit=$_commit")
sha256sums=('SKIP')

prepare() {
    cd "${pkgname}"
}

package() {
    cd "${pkgname}"
    DESTDIR="${pkgdir}" make install
}
