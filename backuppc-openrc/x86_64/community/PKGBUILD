#Maintainer: Nathan Owens <ndowens @ artixlinux.org>

pkgname=backuppc-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC backuppc init script"
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
arch=('any')
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'backuppc')
provides=('init-backuppc')
conflicts=('init-backuppc')
source=('backuppc.initd'
        'backuppc.confd')
sha256sums=('3eb6eac6f2f377febe10192076a1ef280332cf04a3778815bf55a82368f3344c'
            '84b934a34f1ddcff027c9695e6d93a9d2f4de068fa074310ed0d5bc5d21e7f97')

package() {
	install -Dm755 "$srcdir/backuppc.initd" "$pkgdir/etc/init.d/backuppc"
	install -Dm644 "$srcdir/backuppc.confd" "$pkgdir/etc/conf.d/backuppc"
}
