# Maintainer: Rafli Akmal <rafliakmaltejakusuma@gmail.com>
# Contributor: artoo <artoo@artixlinux.org>
# Contributor: Oscar Campos <damnwidget@artixlinux.org>

pkgname=dnscrypt-proxy-openrc
pkgver=20210505
pkgrel=1
pkgdesc="OpenRC dnscrypt-proxy init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'dnscrypt-proxy')
provides=('init-dnscrypt-proxy')
conflicts=('init-dnscrypt-proxy')
source=("dnscrypt-proxy.confd"
        "dnscrypt-proxy.initd")
sha256sums=('fd918f1c0c04e594b8ba50b693b617c8e28562f14e9faa4f1528539d64b2c840'
            '59f5d7e53849aced780142a93ca71f42117d9db3149b5b57d69bef08e64ca92a')

package() {
    install -Dm755 "${srcdir}/dnscrypt-proxy.initd" "${pkgdir}/etc/init.d/dnscrypt-proxy"
    install -Dm644 "${srcdir}/dnscrypt-proxy.confd" "${pkgdir}/etc/conf.d/dnscrypt-proxy"
}
