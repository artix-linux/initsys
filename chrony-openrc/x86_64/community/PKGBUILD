# Maintainer: Nathan Owens <ndowens@artixlinux.org>

pkgname=chrony-openrc
pkgver=20210506
pkgrel=2
pkgdesc="OpenRC chrony init"
arch=('any')
url="https://gitea.artixlinux.org/artixlinux/packages-openrc"
license=('GPL2')
groups=('openrc-galaxy')
provides=('init-chrony' 'init-timed')
depends=('openrc' 'chrony')
conflicts=('init-chrony' 'init-timed')
backup=('etc/conf.d/chrony')
source=("chrony.confd"
        "chrony.initd")
sha256sums=('e65e4cf13bf00d6e7378f86f4513b5b3312b1d8b181bedbef6d8f55e8037f1de'
            '149b12adabd0ab5358de1b3d8674dd5ecde7acd7d14310ee83dae4a72bc84f0b')
b2sums=('496483539b15a55c15287178b7df730fe33fe8d7ceda164f362c0dd6cd833bbee84a0a0496586489659075fc10aafed0f221fb78d60804ddd9edd24e71f6d49b'
        '4e8f80b060bcc7f6f3b0d702f1b85387f6e545c31f315232574bf8ebd5ad2a6604a80a994ba629ffe419776a29339d894f0c1c7db78e9cd6fb4dc4761cf2c398')


package() {
    install -Dm755 "${srcdir}"/chrony.initd "${pkgdir}"/etc/init.d/chrony
    install -Dm644 "${srcdir}"/chrony.confd "${pkgdir}"/etc/conf.d/chrony
}
