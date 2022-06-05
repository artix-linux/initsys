# Maintainer: artoo <artoo@artixlinux.org>

pkgname=nvidia-utils-openrc
pkgver=20210505
pkgrel=2
pkgdesc="OpenRC nvidia persistence daemon init script"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-world')
provides=('init-nvidia-utils')
depends=('openrc' 'nvidia-utils')
conflicts=('init-nvidia-utils')
backup=('etc/conf.d/nvidia-persistenced')
source=("nvidia-persistenced".{confd,initd})
sha256sums=('347437868119e8ae12852a574597936e855f534a9ad290fef3f62b4083a38516'
            'f23eef640cb5a5e499a74bc25cec22a8497d3f8e5853c68264f28a205cdcc7ea')

package() {
    install -Dm755 "$srcdir"/nvidia-persistenced.initd "$pkgdir"/etc/init.d/nvidia-persistenced
    install -Dm644 "$srcdir"/nvidia-persistenced.confd "$pkgdir"/etc/conf.d/nvidia-persistenced
}
