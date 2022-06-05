# Contributor: linuxer <linuxer@artixlinux.org>

pkgname=earlyoom-openrc
pkgver=20210505
pkgrel=1
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
pkgdesc="earlyoom openrc init script"
arch=('x86_64')
license=('GPL2')
groups=('openrc-galaxy')
provides=('init-earlyoom')
depends=('openrc' 'earlyoom')
conflicts=('init-earlyoom')
source=("earlyoom.initd")
b2sums=('9b13d41b7f6fd24f9eb27c34c95d263890440a832b2fabda491e61846adc4ad5acbbcd3f055e0d433c7f4b0ef04741c601a99fb49ca4f9a9695998a827a97aa9')

package(){
    install -Dm755 "${srcdir}"/earlyoom.initd "${pkgdir}"/etc/init.d/earlyoom
}

