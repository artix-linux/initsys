# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=motion-openrc
pkgver=20210505
pkgrel=1
pkgdesc="${pkgname/-openrc/} OpenRC init"
arch=('any')
url="https://gitea.artixlinux.org/PackagesM/motion-openrc"
license=('GPL2')
groups=('openrc-galaxy')
depends=('openrc' 'motion')
provides=('init-motion')
conflicts=('init-motion')
backup=(etc/conf.d/motion)
source=("${pkgname/-openrc/}.initd"
	"${pkgname/-openrc/}.confd")
b2sums=('791a4a840edfcfaedbd38e21cea3d2db2c6048fb23f2b1d97ee82b715aa4c5580e11b5994ed099a639e0da458802098ade645372626fba892957c22f75d45676'
        'fcca520f610cf7a1925c7bbc418c484e209afa1e034b3b6b6f67823385c196d96b89646a729a6b91455be90f0a01d5da92db72dd62153e81d4b277f7d4675dde')

package() {
    install -Dm755 ${srcdir}/motion.initd ${pkgdir}/etc/init.d/motion
    install -Dm644 ${srcdir}/motion.confd ${pkgdir}/etc/conf.d/motion
}
