# Maintainer: Christian Persson <c0r73x at gmail dot com>
pkgname=plcp-git
_gitname=plcp
pkgver=1
pkgrel=1
pkgdesc='Filecopy with progressbar, written in perl'
url=https://github.com/c0r73x
arch=(any)
license=('GPL3')
depends=("perl>=5.10" 'perl-term-readkey' 'perl-config-simple')
makedepends=('git')
conflicts=($_gitname)
provides=($_gitname)

source=("git://github.com/c0r73x/${_gitname}.git")
md5sums=('SKIP')

pkgver() {
  cd "$_gitname"
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {
  cd "$_gitname"

  mkdir -p $pkgdir/usr/bin
  install -C plcp $pkgdir/usr/bin/plcp
}

