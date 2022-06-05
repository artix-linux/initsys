# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=mpd-openrc
pkgver=20210505
pkgrel=2
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-mpd')
depends=('openrc' 'mpd')
conflicts=('init-mpd')
backup=("etc/conf.d/mpd")
source=("mpd".{confd,initd})
sha256sums=('91ef7e00a856dfc78bb79dd5df7908a39a0b315e1f392ba6928ddddac533e25b'
            '375808a86d504c7ec84d92770ac944bc29e3e891f692250d935341c05e403a36')
b2sums=('ae3c582e1bda3a626a753df0927763a34c470997c6acd47ad01bd3e82fe486a4db01164f477c847d1e1b3aa303e5588da6b2361973caa75c3ad8a116f4eacd6b'
        '93e21982b4d6b9e533e2a27f6c819b0ae3486adc07577410345ad8b464aabfc0688e5bf5311e16fe854f238aed938fc08dad089a25baba1de6dfe2307704e5c2')

package() {
    install -Dm755 "${srcdir}"/mpd.initd "${pkgdir}"/etc/init.d/mpd
    install -Dm644 "${srcdir}"/mpd.confd "${pkgdir}"/etc/conf.d/mpd
}
