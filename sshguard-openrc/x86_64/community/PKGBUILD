# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=sshguard-openrc
pkgver=20210505
pkgrel=2
pkgdesc="OpenRC SSHGuard init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'sshguard')
provides=('init-sshguard')
conflicts=('init-sshguard')
backup=('etc/conf.d/sshguard')
source=("sshguard.confd"
        "sshguard.initd")
sha256sums=('ee121f8c4c045ba1cfa67a173040358b1ea5c0561427d64dbd1092a24f068519'
            'de00e9f6cc42542b185e975a23229bddcb31d59c5593ea31f36210119c26f9c9')

package() {
    install -Dm755 "$srcdir/sshguard.initd" "$pkgdir/etc/init.d/sshguard"
    install -Dm644 "$srcdir/sshguard.confd" "$pkgdir/etc/conf.d/sshguard"
}
