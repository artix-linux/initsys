# Maintainer Nathan Owens <ndowens@artixlinux.org>

pkgname=prosody-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC prosody init script"
arch=('any')
url="https://git.alpinelinux.org/aports/tree/community/prosody?h=master"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'prosody')
provides=('init-prosody')
conflicts=('init-prosody')
source=("prosody.initd")
sha256sums=('cf15eb2852b2f6cd75794a7444df49c75fb1cb99afa19e0fe35d60a7a648e4ca')

package() {
  install -Dm755 "$srcdir/prosody.initd" "$pkgdir/etc/init.d/prosody"
}
