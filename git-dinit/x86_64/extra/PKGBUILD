# Maintainer: Muhammad Herdiansyah <koni@artixlinux.org>

pkgname=git-dinit
pkgver=20211030
pkgrel=2
pkgdesc="dinit service scripts for git"
arch=('any')
url="https://artixlinux.org"
license=('BSD')
groups=('dinit-world')
depends=('git' 'dinit')
conflicts=('init-git')
provides=('init-git')
source=("git"
        "git.script")
sha256sums=('73d8101b1a043dcced2cda5332b4a7dda501df77dc91054fce1b78f74f141bc9'
            'e19ebc1854728787d567042fd3dc7c6ae84654b05073acb332c8efcf68164f8d')

package() {
    install -Dm644 git        "$pkgdir/etc/dinit.d/git"
    install -Dm755 git.script "$pkgdir/etc/dinit.d/scripts/git"
}
