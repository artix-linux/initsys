# Maintainer: Nathan Owens <ndowens @ artixlinux.org>

pkgname=stubby-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC Stubby init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'stubby')
provides=('init-stubby')
conflicts=('init-stubby')
backup=('etc/conf.d/stubby')
source=("stubby.confd"
        "stubby.initd"
        "stubby.logrotate")
sha256sums=('d9777a6f3092115566a9c786f929c0d2b3c3a92d2fa78d37e44962acb1133480'
            '74ee9464df93f561b99964285dd446d147590c53a1e763150d7e88e1926a4308'
            '73140697520a1ccdf2096cb2044aacc32ad1c5238973a93d781755c9c8bb6a0d')

package() {
	install -Dm755 "$srcdir/stubby.initd" "$pkgdir/etc/init.d/stubby"
	install -Dm644 "$srcdir/stubby.confd" "$pkgdir/etc/conf.d/stubby"
	install -Dm644 "$srcdir/stubby.logrotate" "$pkgdir/etc/logrotate.d/stubby"
}
