# Maintainer: nous@artixlinux.org

pkgname=spamassassin-openrc
pkgver=20210505
pkgrel=2
pkgdesc="OpenRC spamassassin init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-spamassassin')
depends=('openrc' 'spamassassin')
conflicts=('init-spamassassin')
backup=('etc/conf.d/spamassassin')
source=("spamassassin".{confd,initd})
sha256sums=('94214cef86c5eb6664e5b0af1e31763568caa168941d29a683ce8073510e0b07'
            '0e523efd1efe3171b97f33555e35bacfcc51a05944c457a76864ea4169f39721')

package() {
    install -Dm755 "$srcdir"/spamassassin.initd "$pkgdir"/etc/init.d/spamassassin
    install -Dm644 "$srcdir"/spamassassin.confd "$pkgdir"/etc/conf.d/spamassassin
}
