# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=matrix-synapse-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/PackagesM/matrix-synapse-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'matrix-synapse')
provides=('init-matrix-synapse')
conflicts=('init-matrix-synapse')
backup=("etc/conf.d/${pkgname/-openrc/}")
source=("${pkgname/-openrc/}.initd"
	    "${pkgname/-openrc/}.confd"
	    "matrix_log_config")
b2sums=('bc98b98f7419360b2a815dc92aaff5f8d8bffb4a917a132a510f6f3a9545b9f131ef63575a66b5dcadd7e5083eebd812df06f6ad9f9309e7a66539d92b03b4d9'
        '915a3bae08ac5438df9ef92e6f96ed34c2c4505c783f80341525969f6cb4ee4a42ca70a4b3d39dbad7eecbd56a9f5de510305cada8c64dbfa866dcd419a22637'
        'de58c3d576ba7ca6e8022412c3f3f7d5b0cb42f4db87a72d9f6ddb6157a7909b7db156e3316e4cd47ccaca2e8a4ae80e0610965c1a52e43131e3f1fa84ddd044')

package() {
    install -Dm755 matrix-synapse.initd "$pkgdir"/etc/init.d/matrix-synapse
    install -Dm644 matrix-synapse.confd "$pkgdir"/etc/conf.d/matrix-synapse
    install -Dm644 "$srcdir/matrix_log_config" "$pkgdir/etc/synapse/matrix.log.config"
}
