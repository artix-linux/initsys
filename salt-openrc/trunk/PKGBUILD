# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=salt-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC salt init scripts"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'salt')
provides=('init-salt')
conflicts=('init-salt')
backup=('etc/conf.d/salt-master'
        'etc/conf.d/salt-minion'
        'etc/conf.d/salt-syncdic'
        'etc/conf.d/salt-api')
source=("salt-master.confd"
        "salt-master.initd"
        "salt-minion.confd"
        "salt-minion.initd"
        "salt-syncdic.confd"
        "salt-syncdic.initd"
        "salt-api.confd"
        "salt-api.initd")
sha256sums=('9f3f47a7af4d349a7c525455616139b5019d3b7d0290398ba8c50ab91a62d089'
            '974ef036112514d35569214de0ee079694af1b23311447db5b6755a278a04693'
            '286148f5391d42c04a62a13cc125fa2130b5821e50da913c5a20d3a913e5f2d1'
            'ec686d2b34d567b14fb130022cbfc0be0bce23dfb1f145c96df57668f791c4cd'
            '286148f5391d42c04a62a13cc125fa2130b5821e50da913c5a20d3a913e5f2d1'
            'f427fe683342d8266016438d6779e27d54d525bc64f58b3022cbea8e12726952'
            '9f3f47a7af4d349a7c525455616139b5019d3b7d0290398ba8c50ab91a62d089'
            '7392b5a1ab0c7c480b7d8ff2c32e754530dae62e05049022ff243fa7a5367672')

package() {
  cd "$srcdir"
  for i in *.initd ; do
	install -Dm755 "$i" "$pkgdir/etc/init.d/${i/.initd/}"
  done

  for c in *.confd ; do
	install -Dm644 "$c" "$pkgdir/etc/conf.d/${c/.confd/}"
  done
}
