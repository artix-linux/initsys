# Maintainer: Qontinuum <qontinuum@artixlinux.org>

pkgname=runit-bash-completions
pkgver=1
pkgrel=1
pkgdesc="Runit completions for Bash"
arch=('any')
url="https://artixlinux.org"
depends=('bash-completion')
source=('sv')
sha256sums=('2e6ab7205e1a1782bf671fcece6598ad2df987b02b10ae7cd4fcd4d26ee44b2f')

package() {
    install -Dm644 sv "$pkgdir/usr/share/bash-completion/completions/sv"
}
